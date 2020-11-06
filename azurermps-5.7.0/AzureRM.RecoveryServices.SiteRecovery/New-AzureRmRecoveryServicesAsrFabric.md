---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 53398a882ff513443f8eae336539858f7fe34ce4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531687"
---
# <span data-ttu-id="6e7e2-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6e7e2-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="6e7e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6e7e2-103">Azure Site Recovery 패브릭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e7e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e7e2-104">SYNTAX</span></span>

### <span data-ttu-id="6e7e2-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e7e2-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7e2-106">Azure</span><span class="sxs-lookup"><span data-stu-id="6e7e2-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e7e2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6e7e2-107">DESCRIPTION</span></span>
<span data-ttu-id="6e7e2-108">**AzureRmRecoveryServicesAsrFabric** cmdlet은 지정 된 형식의 Azure Site Recovery Fabric을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="6e7e2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6e7e2-109">EXAMPLES</span></span>

### <span data-ttu-id="6e7e2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e7e2-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="6e7e2-111">전달 된 이름으로 패브릭 만들기를 시작 하 고 패브릭 만들기 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="6e7e2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6e7e2-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="6e7e2-113">전달 된 이름으로 azure fabric 만들기를 시작 하 고 패브릭 만들기 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="6e7e2-114">변수</span><span class="sxs-lookup"><span data-stu-id="6e7e2-114">PARAMETERS</span></span>

### <span data-ttu-id="6e7e2-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="6e7e2-115">-Azure</span></span>
<span data-ttu-id="6e7e2-116">Switch 매개 변수는 azure fabric 만들기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-116">Switch parameter indicates creation of azure fabric.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7e2-117">-확인</span><span class="sxs-lookup"><span data-stu-id="6e7e2-117">-Confirm</span></span>
<span data-ttu-id="6e7e2-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e7e2-119">-DefaultProfile</span></span>
<span data-ttu-id="6e7e2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7e2-121">-위치</span><span class="sxs-lookup"><span data-stu-id="6e7e2-121">-Location</span></span>
<span data-ttu-id="6e7e2-122">만들려는 Fabric 개체에 해당 하는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-122">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="6e7e2-123">Azure Site Recovery fabric 개체는 지역을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-123">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="6e7e2-124">두 Azure 지역 간에 복제 되는 가상 컴퓨터의 기본 패브릭은 기본 Azure 지역 및 복구 패브릭을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-124">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7e2-125">-이름</span><span class="sxs-lookup"><span data-stu-id="6e7e2-125">-Name</span></span>
<span data-ttu-id="6e7e2-126">Azure Site Recovery 패브릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-126">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7e2-127">-Type</span><span class="sxs-lookup"><span data-stu-id="6e7e2-127">-Type</span></span>
<span data-ttu-id="6e7e2-128">Azure Site Recovery 패브릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-128">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e7e2-129">-WhatIf</span></span>
<span data-ttu-id="6e7e2-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e7e2-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e7e2-132">CommonParameters</span></span>
<span data-ttu-id="6e7e2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e7e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e7e2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e7e2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e7e2-135">입력</span><span class="sxs-lookup"><span data-stu-id="6e7e2-135">INPUTS</span></span>

### <span data-ttu-id="6e7e2-136">않아야</span><span class="sxs-lookup"><span data-stu-id="6e7e2-136">None</span></span>

## <span data-ttu-id="6e7e2-137">출력</span><span class="sxs-lookup"><span data-stu-id="6e7e2-137">OUTPUTS</span></span>

### <span data-ttu-id="6e7e2-138">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="6e7e2-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6e7e2-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6e7e2-139">NOTES</span></span>

## <span data-ttu-id="6e7e2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e7e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="6e7e2-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6e7e2-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="6e7e2-142">제거-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6e7e2-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
