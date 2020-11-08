---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212188"
---
# <span data-ttu-id="48f63-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="48f63-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="48f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f63-102">SYNOPSIS</span></span>
<span data-ttu-id="48f63-103">Azure Site Recovery 패브릭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="48f63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48f63-104">SYNTAX</span></span>

### <span data-ttu-id="48f63-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="48f63-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48f63-106">Azure</span><span class="sxs-lookup"><span data-stu-id="48f63-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f63-107">설명은</span><span class="sxs-lookup"><span data-stu-id="48f63-107">DESCRIPTION</span></span>
<span data-ttu-id="48f63-108">**AzRecoveryServicesAsrFabric** cmdlet은 지정 된 형식의 Azure Site Recovery Fabric을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="48f63-109">예제의</span><span class="sxs-lookup"><span data-stu-id="48f63-109">EXAMPLES</span></span>

### <span data-ttu-id="48f63-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="48f63-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="48f63-111">전달 된 이름으로 패브릭 만들기를 시작 하 고 패브릭 만들기 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="48f63-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="48f63-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="48f63-113">전달 된 이름으로 azure fabric 만들기를 시작 하 고 패브릭 만들기 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="48f63-114">변수</span><span class="sxs-lookup"><span data-stu-id="48f63-114">PARAMETERS</span></span>

### <span data-ttu-id="48f63-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="48f63-115">-Azure</span></span>
<span data-ttu-id="48f63-116">Switch 매개 변수는 azure fabric을 만들도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f63-117">-DefaultProfile</span></span>
<span data-ttu-id="48f63-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="48f63-119">-위치</span><span class="sxs-lookup"><span data-stu-id="48f63-119">-Location</span></span>
<span data-ttu-id="48f63-120">만들려는 Fabric 개체에 해당 하는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="48f63-121">Azure Site Recovery fabric 개체는 지역을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="48f63-122">두 Azure 지역 간에 복제 되는 가상 컴퓨터의 기본 패브릭은 기본 Azure 지역 및 복구 패브릭을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f63-123">-이름</span><span class="sxs-lookup"><span data-stu-id="48f63-123">-Name</span></span>
<span data-ttu-id="48f63-124">Azure Site Recovery 패브릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f63-125">-Type</span><span class="sxs-lookup"><span data-stu-id="48f63-125">-Type</span></span>
<span data-ttu-id="48f63-126">Azure Site Recovery 패브릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f63-127">-확인</span><span class="sxs-lookup"><span data-stu-id="48f63-127">-Confirm</span></span>
<span data-ttu-id="48f63-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f63-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f63-129">-WhatIf</span></span>
<span data-ttu-id="48f63-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48f63-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f63-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f63-132">CommonParameters</span></span>
<span data-ttu-id="48f63-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f63-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f63-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="48f63-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f63-135">입력</span><span class="sxs-lookup"><span data-stu-id="48f63-135">INPUTS</span></span>

### <span data-ttu-id="48f63-136">않아야</span><span class="sxs-lookup"><span data-stu-id="48f63-136">None</span></span>

## <span data-ttu-id="48f63-137">출력</span><span class="sxs-lookup"><span data-stu-id="48f63-137">OUTPUTS</span></span>

### <span data-ttu-id="48f63-138">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="48f63-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="48f63-139">상속자</span><span class="sxs-lookup"><span data-stu-id="48f63-139">NOTES</span></span>

## <span data-ttu-id="48f63-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48f63-140">RELATED LINKS</span></span>

[<span data-ttu-id="48f63-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="48f63-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="48f63-142">제거-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="48f63-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
