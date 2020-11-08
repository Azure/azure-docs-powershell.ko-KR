---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046433"
---
# <span data-ttu-id="6467a-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="6467a-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="6467a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6467a-102">SYNOPSIS</span></span>
<span data-ttu-id="6467a-103">사용자에 게 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6467a-103">Sends a message to a user.</span></span>

## <span data-ttu-id="6467a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6467a-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6467a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6467a-105">DESCRIPTION</span></span>
<span data-ttu-id="6467a-106">**AzureRemoteAppSessionMessage** Cmdlet은 Azure RemoteApp 세션에 연결 된 사용자에 게 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6467a-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="6467a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6467a-107">EXAMPLES</span></span>

### <span data-ttu-id="6467a-108">예제 1: 사용자에 게 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="6467a-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="6467a-109">이 명령은 UPN이 있는 사용자에 게 메시지를 보냅니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="6467a-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="6467a-110">변수</span><span class="sxs-lookup"><span data-stu-id="6467a-110">PARAMETERS</span></span>

### <span data-ttu-id="6467a-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="6467a-111">-CollectionName</span></span>
<span data-ttu-id="6467a-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6467a-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6467a-113">-메시지</span><span class="sxs-lookup"><span data-stu-id="6467a-113">-Message</span></span>
<span data-ttu-id="6467a-114">보낼 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6467a-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6467a-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="6467a-115">-Profile</span></span>
<span data-ttu-id="6467a-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6467a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6467a-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6467a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6467a-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="6467a-118">-UserUpn</span></span>
<span data-ttu-id="6467a-119">예를 들어 사용자의 UPN (사용자 계정 이름)을 지정 합니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="6467a-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6467a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6467a-120">CommonParameters</span></span>
<span data-ttu-id="6467a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6467a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6467a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6467a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6467a-123">입력</span><span class="sxs-lookup"><span data-stu-id="6467a-123">INPUTS</span></span>

## <span data-ttu-id="6467a-124">출력</span><span class="sxs-lookup"><span data-stu-id="6467a-124">OUTPUTS</span></span>

## <span data-ttu-id="6467a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="6467a-125">NOTES</span></span>

## <span data-ttu-id="6467a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6467a-126">RELATED LINKS</span></span>

[<span data-ttu-id="6467a-127">추가-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="6467a-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="6467a-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="6467a-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="6467a-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="6467a-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


