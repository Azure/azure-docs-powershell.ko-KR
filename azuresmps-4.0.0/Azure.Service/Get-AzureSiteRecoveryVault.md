---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046565"
---
# <span data-ttu-id="a5d2d-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a5d2d-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="a5d2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d2d-103">현재 구독에서 사이트 복구 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5d2d-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="a5d2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5d2d-104">SYNTAX</span></span>

### <span data-ttu-id="a5d2d-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5d2d-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a5d2d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a5d2d-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a5d2d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5d2d-107">DESCRIPTION</span></span>
<span data-ttu-id="a5d2d-108">**AzureSiteRecoveryVault** cmdlet은 현재 구독에서 Azure site recovery 자격 증명 모음 또는 특정 사이트 복구 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5d2d-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="a5d2d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a5d2d-109">EXAMPLES</span></span>

### <span data-ttu-id="a5d2d-110">예제 1: 활성 자격 증명 모음 가져오기</span><span class="sxs-lookup"><span data-stu-id="a5d2d-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="a5d2d-111">이 명령은 활성 Azure Site Recovery 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5d2d-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a5d2d-112">변수</span><span class="sxs-lookup"><span data-stu-id="a5d2d-112">PARAMETERS</span></span>

### <span data-ttu-id="a5d2d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="a5d2d-113">-Name</span></span>
<span data-ttu-id="a5d2d-114">가져올 저장실의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d2d-114">Specifies the name of the vault to get.</span></span>

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

### <span data-ttu-id="a5d2d-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="a5d2d-115">-Profile</span></span>
<span data-ttu-id="a5d2d-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d2d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5d2d-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d2d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5d2d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d2d-118">CommonParameters</span></span>
<span data-ttu-id="a5d2d-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d2d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d2d-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d2d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d2d-121">입력</span><span class="sxs-lookup"><span data-stu-id="a5d2d-121">INPUTS</span></span>

## <span data-ttu-id="a5d2d-122">출력</span><span class="sxs-lookup"><span data-stu-id="a5d2d-122">OUTPUTS</span></span>

## <span data-ttu-id="a5d2d-123">상속자</span><span class="sxs-lookup"><span data-stu-id="a5d2d-123">NOTES</span></span>

## <span data-ttu-id="a5d2d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5d2d-124">RELATED LINKS</span></span>

[<span data-ttu-id="a5d2d-125">새로운 AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a5d2d-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


