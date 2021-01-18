---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495024"
---
# <span data-ttu-id="7c541-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="7c541-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="7c541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c541-102">SYNOPSIS</span></span>
<span data-ttu-id="7c541-103">규정 준수 표준을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="7c541-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c541-104">SYNTAX</span></span>

### <span data-ttu-id="7c541-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c541-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c541-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7c541-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c541-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c541-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c541-108">설명</span><span class="sxs-lookup"><span data-stu-id="7c541-108">DESCRIPTION</span></span>
<span data-ttu-id="7c541-109">규정 준수 세부 정보를 확인하거나 특정 구독의 모든 규정 준수 표준을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="7c541-110">예제</span><span class="sxs-lookup"><span data-stu-id="7c541-110">EXAMPLES</span></span>

### <span data-ttu-id="7c541-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c541-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="7c541-112">구독에서 모든 규정 준수 표준을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="7c541-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c541-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="7c541-114">표준 이름에 따라 특정 규정 준수 표준에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="7c541-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7c541-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="7c541-116">리소스 ID에 따라 특정 규정 준수 표준에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="7c541-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c541-117">PARAMETERS</span></span>

### <span data-ttu-id="7c541-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c541-118">-DefaultProfile</span></span>
<span data-ttu-id="7c541-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c541-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7c541-120">-Name</span></span>
<span data-ttu-id="7c541-121">표준 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-121">Standard name.</span></span>

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

### <span data-ttu-id="7c541-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c541-122">-ResourceId</span></span>
<span data-ttu-id="7c541-123">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="7c541-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c541-124">CommonParameters</span></span>
<span data-ttu-id="7c541-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c541-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c541-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c541-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c541-127">입력</span><span class="sxs-lookup"><span data-stu-id="7c541-127">INPUTS</span></span>

### <span data-ttu-id="7c541-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7c541-128">System.String</span></span>

## <span data-ttu-id="7c541-129">출력</span><span class="sxs-lookup"><span data-stu-id="7c541-129">OUTPUTS</span></span>

### <span data-ttu-id="7c541-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="7c541-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="7c541-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c541-131">NOTES</span></span>

## <span data-ttu-id="7c541-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c541-132">RELATED LINKS</span></span>
