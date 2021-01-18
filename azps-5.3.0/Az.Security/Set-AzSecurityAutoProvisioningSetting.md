---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494972"
---
# <span data-ttu-id="2ffe2-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="2ffe2-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="2ffe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ffe2-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffe2-103">자동 프로비전 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="2ffe2-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="2ffe2-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ffe2-104">SYNTAX</span></span>

### <span data-ttu-id="2ffe2-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="2ffe2-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ffe2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ffe2-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ffe2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ffe2-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ffe2-108">설명</span><span class="sxs-lookup"><span data-stu-id="2ffe2-108">DESCRIPTION</span></span>
<span data-ttu-id="2ffe2-109">구독에 대한 자동 프로비전 설정을 설정하거나 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="2ffe2-110">자동 프로비전 설정을 사용하면 Azure Security Center에서 VM에 설치할 보안 에이전트를 자동으로 프로비전할지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="2ffe2-111">보안 에이전트는 VM을 모니터링하여 보안 경고를 만들고 VM의 보안 준수를 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="2ffe2-112">예제</span><span class="sxs-lookup"><span data-stu-id="2ffe2-112">EXAMPLES</span></span>

### <span data-ttu-id="2ffe2-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ffe2-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="2ffe2-114">구독에 대한 자동 프로비전 설정을 턴합니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="2ffe2-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="2ffe2-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="2ffe2-116">구독에 대한 자동 프로비전 설정을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="2ffe2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ffe2-117">PARAMETERS</span></span>

### <span data-ttu-id="2ffe2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffe2-118">-DefaultProfile</span></span>
<span data-ttu-id="2ffe2-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ffe2-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="2ffe2-120">-EnableAutoProvision</span></span>
<span data-ttu-id="2ffe2-121">자동 프로비전.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ffe2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ffe2-122">-InputObject</span></span>
<span data-ttu-id="2ffe2-123">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ffe2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2ffe2-124">-Name</span></span>
<span data-ttu-id="2ffe2-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ffe2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ffe2-126">-ResourceId</span></span>
<span data-ttu-id="2ffe2-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ffe2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ffe2-128">-Confirm</span></span>
<span data-ttu-id="2ffe2-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ffe2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ffe2-130">-WhatIf</span></span>
<span data-ttu-id="2ffe2-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2ffe2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ffe2-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ffe2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffe2-133">CommonParameters</span></span>
<span data-ttu-id="2ffe2-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffe2-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ffe2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffe2-136">입력</span><span class="sxs-lookup"><span data-stu-id="2ffe2-136">INPUTS</span></span>

### <span data-ttu-id="2ffe2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2ffe2-137">System.String</span></span>

### <span data-ttu-id="2ffe2-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="2ffe2-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="2ffe2-139">출력</span><span class="sxs-lookup"><span data-stu-id="2ffe2-139">OUTPUTS</span></span>

### <span data-ttu-id="2ffe2-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="2ffe2-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="2ffe2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ffe2-141">NOTES</span></span>

## <span data-ttu-id="2ffe2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ffe2-142">RELATED LINKS</span></span>
