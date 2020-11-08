---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045580"
---
# <span data-ttu-id="e18e6-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="e18e6-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="e18e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e18e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e18e6-103">사이트 복구 자격 증명 모음으로 등록 된 사이트 복구 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="e18e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e18e6-104">SYNTAX</span></span>

### <span data-ttu-id="e18e6-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e18e6-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e18e6-106">ById</span><span class="sxs-lookup"><span data-stu-id="e18e6-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e18e6-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e18e6-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e18e6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e18e6-108">DESCRIPTION</span></span>
<span data-ttu-id="e18e6-109">**AzureSiteRecoveryServer** cmdlet은 현재 사이트 복구 자격 증명 모음에 등록 된 Azure Site recovery 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="e18e6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e18e6-110">EXAMPLES</span></span>

### <span data-ttu-id="e18e6-111">예제 1: 사이트 복구 서버에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="e18e6-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="e18e6-112">이 명령은 Azure Site Recovery 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="e18e6-113">변수</span><span class="sxs-lookup"><span data-stu-id="e18e6-113">PARAMETERS</span></span>

### <span data-ttu-id="e18e6-114">-Id</span><span class="sxs-lookup"><span data-stu-id="e18e6-114">-Id</span></span>
<span data-ttu-id="e18e6-115">서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18e6-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e18e6-116">-Name</span></span>
<span data-ttu-id="e18e6-117">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18e6-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="e18e6-118">-Profile</span></span>
<span data-ttu-id="e18e6-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e18e6-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e18e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18e6-121">CommonParameters</span></span>
<span data-ttu-id="e18e6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e18e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18e6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18e6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18e6-124">입력</span><span class="sxs-lookup"><span data-stu-id="e18e6-124">INPUTS</span></span>

## <span data-ttu-id="e18e6-125">출력</span><span class="sxs-lookup"><span data-stu-id="e18e6-125">OUTPUTS</span></span>

## <span data-ttu-id="e18e6-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e18e6-126">NOTES</span></span>

## <span data-ttu-id="e18e6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e18e6-127">RELATED LINKS</span></span>

[<span data-ttu-id="e18e6-128">Azure Site Recovery 서비스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e18e6-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


