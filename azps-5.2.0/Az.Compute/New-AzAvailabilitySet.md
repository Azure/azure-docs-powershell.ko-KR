---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368831"
---
# <span data-ttu-id="1ecfe-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1ecfe-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="1ecfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ecfe-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecfe-103">Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="1ecfe-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ecfe-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ecfe-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ecfe-105">DESCRIPTION</span></span>
<span data-ttu-id="1ecfe-106">**New-AzAvailabilitySet** cmdlet은 Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="1ecfe-107">예제</span><span class="sxs-lookup"><span data-stu-id="1ecfe-107">EXAMPLES</span></span>

### <span data-ttu-id="1ecfe-108">예제 1: 가용성 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="1ecfe-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="1ecfe-109">이 명령은 ResourceGroup11이라는 리소스 그룹에 AvailabilitySet03이라는 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1ecfe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ecfe-110">PARAMETERS</span></span>

### <span data-ttu-id="1ecfe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ecfe-111">-AsJob</span></span>
<span data-ttu-id="1ecfe-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecfe-113">-DefaultProfile</span></span>
<span data-ttu-id="1ecfe-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ecfe-115">-Location</span><span class="sxs-lookup"><span data-stu-id="1ecfe-115">-Location</span></span>
<span data-ttu-id="1ecfe-116">가용성 집합의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1ecfe-117">-Name</span></span>
<span data-ttu-id="1ecfe-118">가용성 집합의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="1ecfe-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="1ecfe-120">플랫폼 장애 도메인 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="1ecfe-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="1ecfe-122">플랫폼 업데이트 도메인 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="1ecfe-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="1ecfe-124">이 가용성 집합에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecfe-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ecfe-126">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="1ecfe-127">-Sku</span></span>
<span data-ttu-id="1ecfe-128">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-128">The Name of Sku.</span></span>
<span data-ttu-id="1ecfe-129">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1ecfe-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ecfe-130">정렬: 관리 디스크의 경우</span><span class="sxs-lookup"><span data-stu-id="1ecfe-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="1ecfe-131">클래식: 관리되지 않는 디스크의 경우</span><span class="sxs-lookup"><span data-stu-id="1ecfe-131">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ecfe-132">-Tag</span></span>
<span data-ttu-id="1ecfe-133">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-133">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ecfe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecfe-134">CommonParameters</span></span>
<span data-ttu-id="1ecfe-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecfe-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ecfe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecfe-137">입력</span><span class="sxs-lookup"><span data-stu-id="1ecfe-137">INPUTS</span></span>

### <span data-ttu-id="1ecfe-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1ecfe-138">System.String</span></span>

### <span data-ttu-id="1ecfe-139">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1ecfe-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1ecfe-140">출력</span><span class="sxs-lookup"><span data-stu-id="1ecfe-140">OUTPUTS</span></span>

### <span data-ttu-id="1ecfe-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1ecfe-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="1ecfe-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ecfe-142">NOTES</span></span>

## <span data-ttu-id="1ecfe-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ecfe-143">RELATED LINKS</span></span>

[<span data-ttu-id="1ecfe-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1ecfe-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="1ecfe-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1ecfe-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


