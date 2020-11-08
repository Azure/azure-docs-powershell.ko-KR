---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046577"
---
# <span data-ttu-id="59eb4-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="59eb4-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="59eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="59eb4-103">컬렉션에 대 한 모든 활성 및 연결 되지 않은 Azure RemoteApp 세션을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="59eb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59eb4-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="59eb4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="59eb4-106">**AzureRemoteAppSession** Cmdlet은 azure remoteapp 컬렉션에 대 한 모든 활성 및 연결 되지 않은 azure RemoteApp 세션을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="59eb4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="59eb4-108">예제 1: 컬렉션의 모든 세션 나열</span><span class="sxs-lookup"><span data-stu-id="59eb4-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="59eb4-109">이 명령은 ContosoApps 이라는 Azure RemoteApp 컬렉션의 모든 세션을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="59eb4-110">변수</span><span class="sxs-lookup"><span data-stu-id="59eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="59eb4-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="59eb4-111">-CollectionName</span></span>
<span data-ttu-id="59eb4-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="59eb4-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="59eb4-113">-Profile</span></span>
<span data-ttu-id="59eb4-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59eb4-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="59eb4-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="59eb4-116">-UserUpn</span></span>
<span data-ttu-id="59eb4-117">Azure RemoteApp 세션을 가져올 사용자의 UPN (사용자 계정 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="59eb4-118">예를 들어 UPN은 다음 형식이 될 수 있습니다 PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="59eb4-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="59eb4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59eb4-119">CommonParameters</span></span>
<span data-ttu-id="59eb4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59eb4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59eb4-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59eb4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59eb4-122">입력</span><span class="sxs-lookup"><span data-stu-id="59eb4-122">INPUTS</span></span>

## <span data-ttu-id="59eb4-123">출력</span><span class="sxs-lookup"><span data-stu-id="59eb4-123">OUTPUTS</span></span>

## <span data-ttu-id="59eb4-124">상속자</span><span class="sxs-lookup"><span data-stu-id="59eb4-124">NOTES</span></span>

## <span data-ttu-id="59eb4-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59eb4-125">RELATED LINKS</span></span>

[<span data-ttu-id="59eb4-126">연결 해제-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="59eb4-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="59eb4-127">AzureRemoteAppSessionLogoff-호출</span><span class="sxs-lookup"><span data-stu-id="59eb4-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="59eb4-128">송신-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="59eb4-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


