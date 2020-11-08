---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 6c926b606cc764abcf3627c725596deffda395b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044189"
---
# <span data-ttu-id="2d44c-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="2d44c-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="2d44c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d44c-102">SYNOPSIS</span></span>
<span data-ttu-id="2d44c-103">보안 자동 프로 비전 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="2d44c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d44c-104">SYNTAX</span></span>

### <span data-ttu-id="2d44c-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d44c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d44c-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="2d44c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d44c-107">리소스</span><span class="sxs-lookup"><span data-stu-id="2d44c-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d44c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2d44c-108">DESCRIPTION</span></span>
<span data-ttu-id="2d44c-109">자동 프로 비전 설정을 사용 하 여 Azure 보안 센터에서 Vm에 설치 되는 보안 에이전트를 자동으로 프로 비전 할 지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="2d44c-110">보안 에이전트는 VM을 모니터링 하 여 보안 알림을 생성 하 고 VM의 보안 준수를 모니터링 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="2d44c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2d44c-111">EXAMPLES</span></span>

### <span data-ttu-id="2d44c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d44c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="2d44c-113">구독에 대 한 자동 프로비저닝 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="2d44c-114">변수</span><span class="sxs-lookup"><span data-stu-id="2d44c-114">PARAMETERS</span></span>

### <span data-ttu-id="2d44c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d44c-115">-DefaultProfile</span></span>
<span data-ttu-id="2d44c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d44c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="2d44c-117">-Name</span></span>
<span data-ttu-id="2d44c-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-118">Resource name.</span></span>

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

### <span data-ttu-id="2d44c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d44c-119">-ResourceId</span></span>
<span data-ttu-id="2d44c-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-120">Resource ID.</span></span>

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

### <span data-ttu-id="2d44c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d44c-121">CommonParameters</span></span>
<span data-ttu-id="2d44c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d44c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d44c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d44c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d44c-124">입력</span><span class="sxs-lookup"><span data-stu-id="2d44c-124">INPUTS</span></span>

### <span data-ttu-id="2d44c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d44c-125">System.String</span></span>

## <span data-ttu-id="2d44c-126">출력</span><span class="sxs-lookup"><span data-stu-id="2d44c-126">OUTPUTS</span></span>

### <span data-ttu-id="2d44c-127">AutoProvisioningSettings. PSSecurityAutoProvisioningSetting에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="2d44c-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="2d44c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="2d44c-128">NOTES</span></span>

## <span data-ttu-id="2d44c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d44c-129">RELATED LINKS</span></span>
