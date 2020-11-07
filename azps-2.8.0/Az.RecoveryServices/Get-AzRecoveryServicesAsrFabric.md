---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 22e49dc0ebb5c38a1b260f72cc4fe97294bf5505
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872769"
---
# <span data-ttu-id="89455-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="89455-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="89455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89455-102">SYNOPSIS</span></span>
<span data-ttu-id="89455-103">Azure Site Recovery 패브릭의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89455-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="89455-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89455-104">SYNTAX</span></span>

### <span data-ttu-id="89455-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="89455-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89455-106">ByName</span><span class="sxs-lookup"><span data-stu-id="89455-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89455-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="89455-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89455-108">설명은</span><span class="sxs-lookup"><span data-stu-id="89455-108">DESCRIPTION</span></span>
<span data-ttu-id="89455-109">**AzRecoveryServicesAsrFabric** cmdlet은 지정 된 Azure Site recovery 패브릭 또는 복구 서비스 자격 증명 모음의 모든 Azure Site recovery 패브릭에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89455-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="89455-110">예제의</span><span class="sxs-lookup"><span data-stu-id="89455-110">EXAMPLES</span></span>

### <span data-ttu-id="89455-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="89455-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="89455-112">자격 증명 모음의 모든 Azure Site Recovery 패브릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89455-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="89455-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="89455-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="89455-114">이름 xxxx를 사용 하 여 azure site recovery fabric을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89455-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="89455-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="89455-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="89455-116">이름 xxxx를 사용 하 여 azure site recovery fabric을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89455-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="89455-117">변수</span><span class="sxs-lookup"><span data-stu-id="89455-117">PARAMETERS</span></span>

### <span data-ttu-id="89455-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89455-118">-DefaultProfile</span></span>
<span data-ttu-id="89455-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89455-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89455-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="89455-120">-FriendlyName</span></span>
<span data-ttu-id="89455-121">패브릭의 친근 한 이름으로 ASR 패브릭을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="89455-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89455-122">-이름</span><span class="sxs-lookup"><span data-stu-id="89455-122">-Name</span></span>
<span data-ttu-id="89455-123">패브릭 이름으로 ASR 패브릭을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="89455-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89455-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89455-124">CommonParameters</span></span>
<span data-ttu-id="89455-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89455-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89455-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89455-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89455-127">입력</span><span class="sxs-lookup"><span data-stu-id="89455-127">INPUTS</span></span>

### <span data-ttu-id="89455-128">않아야</span><span class="sxs-lookup"><span data-stu-id="89455-128">None</span></span>

## <span data-ttu-id="89455-129">출력</span><span class="sxs-lookup"><span data-stu-id="89455-129">OUTPUTS</span></span>

### <span data-ttu-id="89455-130">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="89455-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="89455-131">상속자</span><span class="sxs-lookup"><span data-stu-id="89455-131">NOTES</span></span>

## <span data-ttu-id="89455-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89455-132">RELATED LINKS</span></span>

[<span data-ttu-id="89455-133">새로운 AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="89455-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="89455-134">제거-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="89455-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
