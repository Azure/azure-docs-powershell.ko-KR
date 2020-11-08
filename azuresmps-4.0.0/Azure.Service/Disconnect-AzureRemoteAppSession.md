---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045686"
---
# <span data-ttu-id="36795-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="36795-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="36795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36795-102">SYNOPSIS</span></span>
<span data-ttu-id="36795-103">Azure RemoteApp 세션의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="36795-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="36795-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36795-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="36795-105">설명은</span><span class="sxs-lookup"><span data-stu-id="36795-105">DESCRIPTION</span></span>
<span data-ttu-id="36795-106">**AzureRemoteAppSession** cmdlet에서 사용자의 Azure RemoteApp 세션 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="36795-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="36795-107">사용자의 클라이언트가 Azure RemoteApp 세션에서 연결을 끊고 사용자의 프로그램이 계속 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36795-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="36795-108">예제의</span><span class="sxs-lookup"><span data-stu-id="36795-108">EXAMPLES</span></span>

### <span data-ttu-id="36795-109">예제 1: 사용자 세션 연결 끊기</span><span class="sxs-lookup"><span data-stu-id="36795-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="36795-110">이 명령은 UPN이 있는 사용자의 ContosoApps 컬렉션에서 Azure RemoteApp 세션의 연결을 끊습니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="36795-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="36795-111">변수</span><span class="sxs-lookup"><span data-stu-id="36795-111">PARAMETERS</span></span>

### <span data-ttu-id="36795-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="36795-112">-CollectionName</span></span>
<span data-ttu-id="36795-113">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36795-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="36795-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="36795-114">-Profile</span></span>
<span data-ttu-id="36795-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36795-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="36795-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="36795-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36795-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="36795-117">-UserUpn</span></span>
<span data-ttu-id="36795-118">예를 들어 사용자의 UPN (사용자 계정 이름)을 지정 합니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="36795-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="36795-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36795-119">CommonParameters</span></span>
<span data-ttu-id="36795-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36795-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36795-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36795-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36795-122">입력</span><span class="sxs-lookup"><span data-stu-id="36795-122">INPUTS</span></span>

## <span data-ttu-id="36795-123">출력</span><span class="sxs-lookup"><span data-stu-id="36795-123">OUTPUTS</span></span>

## <span data-ttu-id="36795-124">상속자</span><span class="sxs-lookup"><span data-stu-id="36795-124">NOTES</span></span>

## <span data-ttu-id="36795-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36795-125">RELATED LINKS</span></span>

[<span data-ttu-id="36795-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="36795-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="36795-127">AzureRemoteAppSessionLogoff-호출</span><span class="sxs-lookup"><span data-stu-id="36795-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="36795-128">송신-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="36795-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


