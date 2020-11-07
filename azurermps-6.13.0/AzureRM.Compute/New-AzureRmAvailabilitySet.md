---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704157"
---
# <span data-ttu-id="4e01a-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4e01a-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="4e01a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e01a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e01a-103">Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e01a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e01a-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e01a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4e01a-105">DESCRIPTION</span></span>
<span data-ttu-id="4e01a-106">**AzureRmAvailabilitySet** Cmdlet은 Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="4e01a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4e01a-107">EXAMPLES</span></span>

### <span data-ttu-id="4e01a-108">예제 1: 가용성 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="4e01a-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="4e01a-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에 AvailablitySet03 이라는 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4e01a-110">변수</span><span class="sxs-lookup"><span data-stu-id="4e01a-110">PARAMETERS</span></span>

### <span data-ttu-id="4e01a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e01a-111">-AsJob</span></span>
<span data-ttu-id="4e01a-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4e01a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e01a-113">-DefaultProfile</span></span>
<span data-ttu-id="4e01a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e01a-115">-위치</span><span class="sxs-lookup"><span data-stu-id="4e01a-115">-Location</span></span>
<span data-ttu-id="4e01a-116">가용성 집합의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="4e01a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4e01a-117">-Name</span></span>
<span data-ttu-id="4e01a-118">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="4e01a-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="4e01a-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="4e01a-120">플랫폼 오류 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="4e01a-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="4e01a-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="4e01a-122">플랫폼 업데이트 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="4e01a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e01a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4e01a-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4e01a-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="4e01a-125">-Sku</span></span>
<span data-ttu-id="4e01a-126">Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-126">The Name of Sku.</span></span>
<span data-ttu-id="4e01a-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e01a-128">맞춤: 관리 디스크</span><span class="sxs-lookup"><span data-stu-id="4e01a-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="4e01a-129">클래식: 관리 되지 않는 디스크</span><span class="sxs-lookup"><span data-stu-id="4e01a-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="4e01a-130">태그</span><span class="sxs-lookup"><span data-stu-id="4e01a-130">-Tag</span></span>
<span data-ttu-id="4e01a-131">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="4e01a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e01a-132">CommonParameters</span></span>
<span data-ttu-id="4e01a-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e01a-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e01a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e01a-135">입력</span><span class="sxs-lookup"><span data-stu-id="4e01a-135">INPUTS</span></span>

### <span data-ttu-id="4e01a-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4e01a-136">System.String</span></span>

### <span data-ttu-id="4e01a-137">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="4e01a-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4e01a-138">출력</span><span class="sxs-lookup"><span data-stu-id="4e01a-138">OUTPUTS</span></span>

### <span data-ttu-id="4e01a-139">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e01a-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="4e01a-140">상속자</span><span class="sxs-lookup"><span data-stu-id="4e01a-140">NOTES</span></span>

## <span data-ttu-id="4e01a-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e01a-141">RELATED LINKS</span></span>

[<span data-ttu-id="4e01a-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4e01a-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="4e01a-143">제거-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4e01a-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


