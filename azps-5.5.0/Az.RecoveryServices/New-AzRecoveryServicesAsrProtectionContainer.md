---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: fecc6f1911a82b20d3f96643ceed83486727f29f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186617"
---
# <span data-ttu-id="4f67a-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4f67a-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="4f67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f67a-102">SYNOPSIS</span></span>
<span data-ttu-id="4f67a-103">지정된 패브릭 내에서 Azure Site Recovery Protection 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="4f67a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f67a-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f67a-105">설명</span><span class="sxs-lookup"><span data-stu-id="4f67a-105">DESCRIPTION</span></span>
<span data-ttu-id="4f67a-106">이 New-AzRecoveryServicesAsrProtectionContainer cmdlet은 지정된 Azure Site Recovery Fabric 아래에 보호 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="4f67a-107">예제</span><span class="sxs-lookup"><span data-stu-id="4f67a-107">EXAMPLES</span></span>

### <span data-ttu-id="4f67a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f67a-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="4f67a-109">지정된 매개 변수를 사용하여 보호 컨테이너 만들기를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4f67a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f67a-110">PARAMETERS</span></span>

### <span data-ttu-id="4f67a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f67a-111">-DefaultProfile</span></span>
<span data-ttu-id="4f67a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f67a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f67a-113">-InputObject</span></span>
<span data-ttu-id="4f67a-114">지정된 입력 개체(Azure Fabric)에 복제 보호 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f67a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4f67a-115">-Name</span></span>
<span data-ttu-id="4f67a-116">보호 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="4f67a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f67a-117">-Confirm</span></span>
<span data-ttu-id="4f67a-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f67a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f67a-119">-WhatIf</span></span>
<span data-ttu-id="4f67a-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4f67a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f67a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f67a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f67a-122">CommonParameters</span></span>
<span data-ttu-id="4f67a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f67a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f67a-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f67a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f67a-125">입력</span><span class="sxs-lookup"><span data-stu-id="4f67a-125">INPUTS</span></span>

### <span data-ttu-id="4f67a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4f67a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4f67a-127">출력</span><span class="sxs-lookup"><span data-stu-id="4f67a-127">OUTPUTS</span></span>

### <span data-ttu-id="4f67a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4f67a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4f67a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f67a-129">NOTES</span></span>

## <span data-ttu-id="4f67a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f67a-130">RELATED LINKS</span></span>
