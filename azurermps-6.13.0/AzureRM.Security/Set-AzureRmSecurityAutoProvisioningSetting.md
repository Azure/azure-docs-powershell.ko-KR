---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702580"
---
# <span data-ttu-id="5d5c1-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="5d5c1-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="5d5c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5c1-103">업데이트 자동 프로비저닝 설정</span><span class="sxs-lookup"><span data-stu-id="5d5c1-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d5c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d5c1-104">SYNTAX</span></span>

### <span data-ttu-id="5d5c1-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="5d5c1-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d5c1-106">리소스</span><span class="sxs-lookup"><span data-stu-id="5d5c1-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d5c1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5d5c1-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d5c1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5d5c1-108">DESCRIPTION</span></span>
<span data-ttu-id="5d5c1-109">구독에 대 한 자동 프로비저닝 설정을 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="5d5c1-110">자동 프로 비전 설정을 사용 하 여 Azure 보안 센터에서 Vm에 설치 되는 보안 에이전트를 자동으로 프로 비전 할 지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="5d5c1-111">보안 에이전트는 VM을 모니터링 하 여 보안 알림을 생성 하 고 VM의 보안 준수를 모니터링 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="5d5c1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5d5c1-112">EXAMPLES</span></span>

### <span data-ttu-id="5d5c1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d5c1-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="5d5c1-114">구독에 대 한 자동 프로 비전 설정을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="5d5c1-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="5d5c1-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="5d5c1-116">구독에 대 한 자동 프로비저닝 설정을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="5d5c1-117">변수</span><span class="sxs-lookup"><span data-stu-id="5d5c1-117">PARAMETERS</span></span>

### <span data-ttu-id="5d5c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5c1-118">-DefaultProfile</span></span>
<span data-ttu-id="5d5c1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d5c1-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="5d5c1-120">-EnableAutoProvision</span></span>
<span data-ttu-id="5d5c1-121">자동 프로비저닝.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5c1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d5c1-122">-InputObject</span></span>
<span data-ttu-id="5d5c1-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="5d5c1-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5c1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="5d5c1-124">-Name</span></span>
<span data-ttu-id="5d5c1-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5c1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d5c1-126">-ResourceId</span></span>
<span data-ttu-id="5d5c1-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5c1-128">-확인</span><span class="sxs-lookup"><span data-stu-id="5d5c1-128">-Confirm</span></span>
<span data-ttu-id="5d5c1-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5c1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5c1-130">-WhatIf</span></span>
<span data-ttu-id="5d5c1-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d5c1-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5c1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5c1-133">CommonParameters</span></span>
<span data-ttu-id="5d5c1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5c1-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5c1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5c1-136">입력</span><span class="sxs-lookup"><span data-stu-id="5d5c1-136">INPUTS</span></span>

### <span data-ttu-id="5d5c1-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d5c1-137">System.String</span></span>
<span data-ttu-id="5d5c1-138">AutoProvisioningSettings. PSSecurityAutoProvisioningSetting에는 system.webserver 매개 변수.. m m.</span><span class="sxs-lookup"><span data-stu-id="5d5c1-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="5d5c1-139">출력</span><span class="sxs-lookup"><span data-stu-id="5d5c1-139">OUTPUTS</span></span>

### <span data-ttu-id="5d5c1-140">AutoProvisioningSettings. PSSecurityAutoProvisioningSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="5d5c1-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="5d5c1-141">상속자</span><span class="sxs-lookup"><span data-stu-id="5d5c1-141">NOTES</span></span>

## <span data-ttu-id="5d5c1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d5c1-142">RELATED LINKS</span></span>
