---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212422"
---
# <span data-ttu-id="e8cc1-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8cc1-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="e8cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cc1-103">Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="e8cc1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8cc1-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8cc1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="e8cc1-106">**AzAvailabilitySet** Cmdlet은 Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="e8cc1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e8cc1-107">EXAMPLES</span></span>

### <span data-ttu-id="e8cc1-108">예제 1: 가용성 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="e8cc1-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="e8cc1-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에 AvailabilitySet03 이라는 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e8cc1-110">변수</span><span class="sxs-lookup"><span data-stu-id="e8cc1-110">PARAMETERS</span></span>

### <span data-ttu-id="e8cc1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8cc1-111">-AsJob</span></span>
<span data-ttu-id="e8cc1-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e8cc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cc1-113">-DefaultProfile</span></span>
<span data-ttu-id="e8cc1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8cc1-115">-위치</span><span class="sxs-lookup"><span data-stu-id="e8cc1-115">-Location</span></span>
<span data-ttu-id="e8cc1-116">가용성 집합의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="e8cc1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e8cc1-117">-Name</span></span>
<span data-ttu-id="e8cc1-118">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="e8cc1-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="e8cc1-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="e8cc1-120">플랫폼 오류 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="e8cc1-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="e8cc1-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="e8cc1-122">플랫폼 업데이트 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="e8cc1-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e8cc1-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e8cc1-124">이 가용성 집합에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="e8cc1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cc1-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8cc1-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e8cc1-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="e8cc1-127">-Sku</span></span>
<span data-ttu-id="e8cc1-128">Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-128">The Name of Sku.</span></span>
<span data-ttu-id="e8cc1-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e8cc1-130">맞춤: 관리 디스크</span><span class="sxs-lookup"><span data-stu-id="e8cc1-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="e8cc1-131">클래식: 관리 되지 않는 디스크</span><span class="sxs-lookup"><span data-stu-id="e8cc1-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="e8cc1-132">태그</span><span class="sxs-lookup"><span data-stu-id="e8cc1-132">-Tag</span></span>
<span data-ttu-id="e8cc1-133">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="e8cc1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cc1-134">CommonParameters</span></span>
<span data-ttu-id="e8cc1-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cc1-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cc1-137">입력</span><span class="sxs-lookup"><span data-stu-id="e8cc1-137">INPUTS</span></span>

### <span data-ttu-id="e8cc1-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e8cc1-138">System.String</span></span>

### <span data-ttu-id="e8cc1-139">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="e8cc1-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e8cc1-140">출력</span><span class="sxs-lookup"><span data-stu-id="e8cc1-140">OUTPUTS</span></span>

### <span data-ttu-id="e8cc1-141">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8cc1-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e8cc1-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e8cc1-142">NOTES</span></span>

## <span data-ttu-id="e8cc1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8cc1-143">RELATED LINKS</span></span>

[<span data-ttu-id="e8cc1-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8cc1-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="e8cc1-145">제거-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8cc1-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


