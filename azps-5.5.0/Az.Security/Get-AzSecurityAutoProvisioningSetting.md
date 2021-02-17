---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197932"
---
# <span data-ttu-id="36b51-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="36b51-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="36b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b51-102">SYNOPSIS</span></span>
<span data-ttu-id="36b51-103">보안 자동 프로비전 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="36b51-104">구문</span><span class="sxs-lookup"><span data-stu-id="36b51-104">SYNTAX</span></span>

### <span data-ttu-id="36b51-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="36b51-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36b51-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="36b51-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36b51-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b51-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36b51-108">설명</span><span class="sxs-lookup"><span data-stu-id="36b51-108">DESCRIPTION</span></span>
<span data-ttu-id="36b51-109">자동 프로비전 설정을 사용하면 Azure Security Center에서 VM에 설치할 보안 에이전트를 자동으로 프로비전할지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="36b51-110">보안 에이전트는 VM을 모니터링하여 보안 경고를 만들고 VM의 보안 준수를 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="36b51-111">예제</span><span class="sxs-lookup"><span data-stu-id="36b51-111">EXAMPLES</span></span>

### <span data-ttu-id="36b51-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="36b51-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="36b51-113">구독에 대한 자동 프로비전 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="36b51-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b51-114">PARAMETERS</span></span>

### <span data-ttu-id="36b51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b51-115">-DefaultProfile</span></span>
<span data-ttu-id="36b51-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b51-117">-Name</span><span class="sxs-lookup"><span data-stu-id="36b51-117">-Name</span></span>
<span data-ttu-id="36b51-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-118">Resource name.</span></span>

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

### <span data-ttu-id="36b51-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b51-119">-ResourceId</span></span>
<span data-ttu-id="36b51-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-120">Resource ID.</span></span>

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

### <span data-ttu-id="36b51-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b51-121">CommonParameters</span></span>
<span data-ttu-id="36b51-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36b51-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b51-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36b51-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b51-124">입력</span><span class="sxs-lookup"><span data-stu-id="36b51-124">INPUTS</span></span>

### <span data-ttu-id="36b51-125">System.String</span><span class="sxs-lookup"><span data-stu-id="36b51-125">System.String</span></span>

## <span data-ttu-id="36b51-126">출력</span><span class="sxs-lookup"><span data-stu-id="36b51-126">OUTPUTS</span></span>

### <span data-ttu-id="36b51-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="36b51-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="36b51-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36b51-128">NOTES</span></span>

## <span data-ttu-id="36b51-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36b51-129">RELATED LINKS</span></span>
