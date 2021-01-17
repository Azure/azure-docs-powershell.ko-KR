---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490768"
---
# <span data-ttu-id="74f8e-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="74f8e-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="74f8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="74f8e-103">Azure Site Recovery 보호 컨테이너 매핑을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="74f8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="74f8e-104">SYNTAX</span></span>

### <span data-ttu-id="74f8e-105">AzureToAzureEnableAutoUpdate(기본값)</span><span class="sxs-lookup"><span data-stu-id="74f8e-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f8e-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="74f8e-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74f8e-107">설명</span><span class="sxs-lookup"><span data-stu-id="74f8e-107">DESCRIPTION</span></span>
<span data-ttu-id="74f8e-108">**Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정된 Azure Site Recovery 보호 컨테이너 매핑을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="74f8e-109">예제</span><span class="sxs-lookup"><span data-stu-id="74f8e-109">EXAMPLES</span></span>

### <span data-ttu-id="74f8e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="74f8e-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="74f8e-111">컨테이너에 대한 자동 업데이트를 사용하지 않도록 설정하는 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="74f8e-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="74f8e-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="74f8e-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="74f8e-113">컨테이너에 대한 자동 업데이트를 사용하지 않도록 설정하는 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="74f8e-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="74f8e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f8e-114">PARAMETERS</span></span>

### <span data-ttu-id="74f8e-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="74f8e-115">-AutomationAccountId</span></span>
<span data-ttu-id="74f8e-116">자동 udpate에 사용되는 automation accountId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f8e-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="74f8e-117">-AzureToAzure</span></span>
<span data-ttu-id="74f8e-118">Azure-Azure 보호 컨테이너를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f8e-119">-DefaultProfile</span></span>
<span data-ttu-id="74f8e-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f8e-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="74f8e-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="74f8e-122">자동 업데이트를 사용하지 않도록 매개 변수를 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f8e-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="74f8e-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="74f8e-124">매개 변수를 전환하여 자동 업데이트를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f8e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74f8e-125">-InputObject</span></span>
<span data-ttu-id="74f8e-126">보호 컨테이너 매핑에 대한 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74f8e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74f8e-127">-Confirm</span></span>
<span data-ttu-id="74f8e-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f8e-129">-WhatIf</span></span>
<span data-ttu-id="74f8e-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="74f8e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f8e-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f8e-132">CommonParameters</span></span>
<span data-ttu-id="74f8e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74f8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f8e-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74f8e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f8e-135">입력</span><span class="sxs-lookup"><span data-stu-id="74f8e-135">INPUTS</span></span>

### <span data-ttu-id="74f8e-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="74f8e-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="74f8e-137">출력</span><span class="sxs-lookup"><span data-stu-id="74f8e-137">OUTPUTS</span></span>

### <span data-ttu-id="74f8e-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="74f8e-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="74f8e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74f8e-139">NOTES</span></span>

## <span data-ttu-id="74f8e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74f8e-140">RELATED LINKS</span></span>
