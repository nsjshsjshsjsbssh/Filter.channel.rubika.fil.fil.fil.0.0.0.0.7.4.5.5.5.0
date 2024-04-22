if($update->chat_member->new_chat_member->status == "left"){
bot('KickChatMember',[
'chat_id'=>$update->chat_member->chat->id,
'user_id'=>$update->chat_member->new_chat_member->user->id,
]);
bot('sendmessage',[
'chat_id'=>$update->chat_member->chat->id,
"text"=>"یک نفر کانال را ترک کرد و بن شد: \n نام: ".$update->chat_member->new_chat_member->user->first_name,
]);
}
