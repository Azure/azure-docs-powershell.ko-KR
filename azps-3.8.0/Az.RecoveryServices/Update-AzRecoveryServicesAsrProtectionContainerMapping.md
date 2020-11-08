---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034269"
---
# <span data-ttu-id="1db0d-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1db0d-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="1db0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db0d-102">SYNOPSIS</span></span>
<span data-ttu-id="1db0d-103">Azure site recovery 보호 컨테이너 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="1db0d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1db0d-104">SYNTAX</span></span>

### <span data-ttu-id="1db0d-105">AzureToAzureEnableAutoUpdate 업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1db0d-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db0d-106">AzureToAzureDisableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="1db0d-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1db0d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1db0d-107">DESCRIPTION</span></span>
<span data-ttu-id="1db0d-108">**업데이트 AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 Azure Site Recovery 보호 컨테이너 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="1db0d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1db0d-109">EXAMPLES</span></span>

### <span data-ttu-id="1db0d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1db0d-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="1db0d-111">컨테이너에 대 한 자동 업데이트를 해제 하려면 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="1db0d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1db0d-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="1db0d-113">컨테이너에 자동 업데이트 사용을 사용 하지 않도록 설정 하려면 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="1db0d-114">변수</span><span class="sxs-lookup"><span data-stu-id="1db0d-114">PARAMETERS</span></span>

### <span data-ttu-id="1db0d-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="1db0d-115">-AutomationAccountId</span></span>
<span data-ttu-id="1db0d-116">자동 udpate에 사용 되는 자동화 accountId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="1db0d-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="1db0d-117">-AzureToAzure</span></span>
<span data-ttu-id="1db0d-118">Azure에서 Azure 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="1db0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db0d-119">-DefaultProfile</span></span>
<span data-ttu-id="1db0d-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1db0d-121">-DisableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="1db0d-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="1db0d-122">스위치 매개 변수를 사용 하 여 자동 업데이트를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="1db0d-123">-EnableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="1db0d-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="1db0d-124">자동 업데이트를 사용 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="1db0d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1db0d-125">-InputObject</span></span>
<span data-ttu-id="1db0d-126">보호 컨테이너 매핑에 대 한 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="1db0d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="1db0d-127">-Confirm</span></span>
<span data-ttu-id="1db0d-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db0d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db0d-129">-WhatIf</span></span>
<span data-ttu-id="1db0d-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1db0d-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1db0d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db0d-132">CommonParameters</span></span>
<span data-ttu-id="1db0d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1db0d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db0d-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1db0d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db0d-135">입력</span><span class="sxs-lookup"><span data-stu-id="1db0d-135">INPUTS</span></span>

### <span data-ttu-id="1db0d-136">SiteRecovery. ASRProtectionContainerMapping에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="1db0d-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="1db0d-137">출력</span><span class="sxs-lookup"><span data-stu-id="1db0d-137">OUTPUTS</span></span>

### <span data-ttu-id="1db0d-138">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="1db0d-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1db0d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1db0d-139">NOTES</span></span>

## <span data-ttu-id="1db0d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1db0d-140">RELATED LINKS</span></span>
