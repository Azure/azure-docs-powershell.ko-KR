---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: d4741bc0456abfe99071f57d3224db8925bd1724
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699228"
---
# <span data-ttu-id="d339d-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="d339d-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d339d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d339d-102">SYNOPSIS</span></span>
<span data-ttu-id="d339d-103">업데이트 자동 프로비저닝 설정</span><span class="sxs-lookup"><span data-stu-id="d339d-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="d339d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d339d-104">SYNTAX</span></span>

### <span data-ttu-id="d339d-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="d339d-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d339d-106">리소스</span><span class="sxs-lookup"><span data-stu-id="d339d-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d339d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d339d-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d339d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d339d-108">DESCRIPTION</span></span>
<span data-ttu-id="d339d-109">구독에 대 한 자동 프로비저닝 설정을 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="d339d-110">자동 프로 비전 설정을 사용 하 여 Azure 보안 센터에서 Vm에 설치 되는 보안 에이전트를 자동으로 프로 비전 할 지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="d339d-111">보안 에이전트는 VM을 모니터링 하 여 보안 알림을 생성 하 고 VM의 보안 준수를 모니터링 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="d339d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d339d-112">EXAMPLES</span></span>

### <span data-ttu-id="d339d-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d339d-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="d339d-114">구독에 대 한 자동 프로 비전 설정을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="d339d-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="d339d-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="d339d-116">구독에 대 한 자동 프로비저닝 설정을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="d339d-117">변수</span><span class="sxs-lookup"><span data-stu-id="d339d-117">PARAMETERS</span></span>

### <span data-ttu-id="d339d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d339d-118">-DefaultProfile</span></span>
<span data-ttu-id="d339d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d339d-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="d339d-120">-EnableAutoProvision</span></span>
<span data-ttu-id="d339d-121">자동 프로비저닝.</span><span class="sxs-lookup"><span data-stu-id="d339d-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="d339d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d339d-122">-InputObject</span></span>
<span data-ttu-id="d339d-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="d339d-123">Input Object.</span></span>

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

### <span data-ttu-id="d339d-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d339d-124">-Name</span></span>
<span data-ttu-id="d339d-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-125">Resource name.</span></span>

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

### <span data-ttu-id="d339d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d339d-126">-ResourceId</span></span>
<span data-ttu-id="d339d-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-127">Resource ID.</span></span>

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

### <span data-ttu-id="d339d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d339d-128">-Confirm</span></span>
<span data-ttu-id="d339d-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d339d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d339d-130">-WhatIf</span></span>
<span data-ttu-id="d339d-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d339d-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d339d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d339d-133">CommonParameters</span></span>
<span data-ttu-id="d339d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d339d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d339d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d339d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d339d-136">입력</span><span class="sxs-lookup"><span data-stu-id="d339d-136">INPUTS</span></span>

### <span data-ttu-id="d339d-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d339d-137">System.String</span></span>

### <span data-ttu-id="d339d-138">AutoProvisioningSettings. PSSecurityAutoProvisioningSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="d339d-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d339d-139">출력</span><span class="sxs-lookup"><span data-stu-id="d339d-139">OUTPUTS</span></span>

### <span data-ttu-id="d339d-140">AutoProvisioningSettings. PSSecurityAutoProvisioningSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="d339d-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d339d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d339d-141">NOTES</span></span>

## <span data-ttu-id="d339d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d339d-142">RELATED LINKS</span></span>