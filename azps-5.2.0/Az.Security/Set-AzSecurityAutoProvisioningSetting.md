---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335414"
---
# <span data-ttu-id="cd19e-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="cd19e-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="cd19e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd19e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd19e-103">자동 프로비전 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="cd19e-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="cd19e-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd19e-104">SYNTAX</span></span>

### <span data-ttu-id="cd19e-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd19e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd19e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd19e-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd19e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cd19e-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd19e-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd19e-108">DESCRIPTION</span></span>
<span data-ttu-id="cd19e-109">구독에 대한 자동 프로비전 설정을 설정하거나 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="cd19e-110">자동 프로비전 설정을 사용하면 Azure Security Center에서 VM에 설치할 보안 에이전트를 자동으로 프로비전할지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="cd19e-111">보안 에이전트는 VM을 모니터링하여 보안 경고를 만들고 VM의 보안 준수를 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="cd19e-112">예제</span><span class="sxs-lookup"><span data-stu-id="cd19e-112">EXAMPLES</span></span>

### <span data-ttu-id="cd19e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd19e-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="cd19e-114">구독에 대한 자동 프로비전 설정을 턴합니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="cd19e-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="cd19e-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="cd19e-116">구독에 대한 자동 프로비전 설정을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="cd19e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd19e-117">PARAMETERS</span></span>

### <span data-ttu-id="cd19e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd19e-118">-DefaultProfile</span></span>
<span data-ttu-id="cd19e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd19e-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="cd19e-120">-EnableAutoProvision</span></span>
<span data-ttu-id="cd19e-121">자동 프로비전.</span><span class="sxs-lookup"><span data-stu-id="cd19e-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="cd19e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd19e-122">-InputObject</span></span>
<span data-ttu-id="cd19e-123">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-123">Input Object.</span></span>

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

### <span data-ttu-id="cd19e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cd19e-124">-Name</span></span>
<span data-ttu-id="cd19e-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-125">Resource name.</span></span>

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

### <span data-ttu-id="cd19e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd19e-126">-ResourceId</span></span>
<span data-ttu-id="cd19e-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-127">Resource ID.</span></span>

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

### <span data-ttu-id="cd19e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd19e-128">-Confirm</span></span>
<span data-ttu-id="cd19e-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd19e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd19e-130">-WhatIf</span></span>
<span data-ttu-id="cd19e-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cd19e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd19e-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd19e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd19e-133">CommonParameters</span></span>
<span data-ttu-id="cd19e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd19e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd19e-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd19e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd19e-136">입력</span><span class="sxs-lookup"><span data-stu-id="cd19e-136">INPUTS</span></span>

### <span data-ttu-id="cd19e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cd19e-137">System.String</span></span>

### <span data-ttu-id="cd19e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="cd19e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="cd19e-139">출력</span><span class="sxs-lookup"><span data-stu-id="cd19e-139">OUTPUTS</span></span>

### <span data-ttu-id="cd19e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="cd19e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="cd19e-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd19e-141">NOTES</span></span>

## <span data-ttu-id="cd19e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd19e-142">RELATED LINKS</span></span>
