---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348045"
---
# <span data-ttu-id="ae281-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ae281-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="ae281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae281-102">SYNOPSIS</span></span>
<span data-ttu-id="ae281-103">Azure Site Recovery 패브릭의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="ae281-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae281-104">SYNTAX</span></span>

### <span data-ttu-id="ae281-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="ae281-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae281-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ae281-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae281-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ae281-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae281-108">설명</span><span class="sxs-lookup"><span data-stu-id="ae281-108">DESCRIPTION</span></span>
<span data-ttu-id="ae281-109">**Get-AzRecoveryServicesAsrFabric** cmdlet은 지정된 Azure Site Recovery Fabric 또는 Recovery Service 자격 증명 모음의 모든 Azure Site Recovery Fabric의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="ae281-110">예제</span><span class="sxs-lookup"><span data-stu-id="ae281-110">EXAMPLES</span></span>

### <span data-ttu-id="ae281-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae281-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="ae281-112">자격 증명 모음의 모든 Azure Site Recovery 패브릭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="ae281-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ae281-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="ae281-114">이름이 xxxx인 Azure Site Recovery 패브릭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="ae281-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="ae281-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="ae281-116">친숙한 이름 xxxx를 사용하여 Azure Site Recovery 패브릭을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="ae281-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae281-117">PARAMETERS</span></span>

### <span data-ttu-id="ae281-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae281-118">-DefaultProfile</span></span>
<span data-ttu-id="ae281-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae281-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ae281-120">-FriendlyName</span></span>
<span data-ttu-id="ae281-121">패브릭의 이름을 사용하여 ASR 패브릭을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="ae281-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ae281-122">-Name</span></span>
<span data-ttu-id="ae281-123">패브릭 이름으로 ASR 패브릭을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="ae281-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae281-124">CommonParameters</span></span>
<span data-ttu-id="ae281-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae281-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae281-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae281-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae281-127">입력</span><span class="sxs-lookup"><span data-stu-id="ae281-127">INPUTS</span></span>

### <span data-ttu-id="ae281-128">없음</span><span class="sxs-lookup"><span data-stu-id="ae281-128">None</span></span>

## <span data-ttu-id="ae281-129">출력</span><span class="sxs-lookup"><span data-stu-id="ae281-129">OUTPUTS</span></span>

### <span data-ttu-id="ae281-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ae281-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ae281-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae281-131">NOTES</span></span>

## <span data-ttu-id="ae281-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae281-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae281-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ae281-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="ae281-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ae281-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
