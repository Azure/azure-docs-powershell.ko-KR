---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214244"
---
# <span data-ttu-id="eb18f-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb18f-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="eb18f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb18f-102">SYNOPSIS</span></span>
<span data-ttu-id="eb18f-103">Azure site recovery 보호 컨테이너 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="eb18f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb18f-104">SYNTAX</span></span>

### <span data-ttu-id="eb18f-105">AzureToAzureEnableAutoUpdate 업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb18f-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb18f-106">AzureToAzureDisableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="eb18f-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb18f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eb18f-107">DESCRIPTION</span></span>
<span data-ttu-id="eb18f-108">**업데이트 AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 Azure Site Recovery 보호 컨테이너 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="eb18f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eb18f-109">EXAMPLES</span></span>

### <span data-ttu-id="eb18f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="eb18f-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="eb18f-111">컨테이너에 대 한 자동 업데이트를 해제 하려면 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="eb18f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="eb18f-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="eb18f-113">컨테이너에 자동 업데이트 사용을 사용 하지 않도록 설정 하려면 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="eb18f-114">변수</span><span class="sxs-lookup"><span data-stu-id="eb18f-114">PARAMETERS</span></span>

### <span data-ttu-id="eb18f-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="eb18f-115">-AutomationAccountId</span></span>
<span data-ttu-id="eb18f-116">자동 udpate에 사용 되는 자동화 accountId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="eb18f-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="eb18f-117">-AzureToAzure</span></span>
<span data-ttu-id="eb18f-118">Azure에서 Azure 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="eb18f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb18f-119">-DefaultProfile</span></span>
<span data-ttu-id="eb18f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb18f-121">-DisableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="eb18f-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="eb18f-122">스위치 매개 변수를 사용 하 여 자동 업데이트를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="eb18f-123">-EnableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="eb18f-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="eb18f-124">자동 업데이트를 사용 하는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="eb18f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb18f-125">-InputObject</span></span>
<span data-ttu-id="eb18f-126">보호 컨테이너 매핑에 대 한 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="eb18f-127">-확인</span><span class="sxs-lookup"><span data-stu-id="eb18f-127">-Confirm</span></span>
<span data-ttu-id="eb18f-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb18f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb18f-129">-WhatIf</span></span>
<span data-ttu-id="eb18f-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb18f-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb18f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb18f-132">CommonParameters</span></span>
<span data-ttu-id="eb18f-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb18f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb18f-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eb18f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb18f-135">입력</span><span class="sxs-lookup"><span data-stu-id="eb18f-135">INPUTS</span></span>

### <span data-ttu-id="eb18f-136">SiteRecovery. ASRProtectionContainerMapping에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="eb18f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="eb18f-137">출력</span><span class="sxs-lookup"><span data-stu-id="eb18f-137">OUTPUTS</span></span>

### <span data-ttu-id="eb18f-138">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="eb18f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eb18f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="eb18f-139">NOTES</span></span>

## <span data-ttu-id="eb18f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb18f-140">RELATED LINKS</span></span>
