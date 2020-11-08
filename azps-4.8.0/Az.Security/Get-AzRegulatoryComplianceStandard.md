---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213987"
---
# <span data-ttu-id="4775b-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="4775b-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="4775b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4775b-102">SYNOPSIS</span></span>
<span data-ttu-id="4775b-103">Regulatoey 준수 표준을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4775b-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="4775b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4775b-104">SYNTAX</span></span>

### <span data-ttu-id="4775b-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4775b-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4775b-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="4775b-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4775b-107">리소스</span><span class="sxs-lookup"><span data-stu-id="4775b-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4775b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4775b-108">DESCRIPTION</span></span>
<span data-ttu-id="4775b-109">Spcific 규제 준수 satandard 세부 정보를 확인 하거나 특정 구독에서 모든 규정 준수 표준을 나열 하세요.</span><span class="sxs-lookup"><span data-stu-id="4775b-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="4775b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4775b-110">EXAMPLES</span></span>

### <span data-ttu-id="4775b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4775b-111">Example 1</span></span>
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

<span data-ttu-id="4775b-112">구독 하는 모든 규정 준수 표준을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="4775b-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="4775b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4775b-113">Example 2</span></span>
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

<span data-ttu-id="4775b-114">표준 이름에 따라 특정 규제 준수 표준에 대 한 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="4775b-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="4775b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="4775b-115">Example 3</span></span>
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

<span data-ttu-id="4775b-116">리소스 id에 따라 특정 규제 준수 표준에 대 한 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="4775b-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="4775b-117">변수</span><span class="sxs-lookup"><span data-stu-id="4775b-117">PARAMETERS</span></span>

### <span data-ttu-id="4775b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4775b-118">-DefaultProfile</span></span>
<span data-ttu-id="4775b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4775b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4775b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4775b-120">-Name</span></span>
<span data-ttu-id="4775b-121">표준 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4775b-121">Standard name.</span></span>

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

### <span data-ttu-id="4775b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4775b-122">-ResourceId</span></span>
<span data-ttu-id="4775b-123">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4775b-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="4775b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4775b-124">CommonParameters</span></span>
<span data-ttu-id="4775b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4775b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4775b-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4775b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4775b-127">입력</span><span class="sxs-lookup"><span data-stu-id="4775b-127">INPUTS</span></span>

### <span data-ttu-id="4775b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4775b-128">System.String</span></span>

## <span data-ttu-id="4775b-129">출력</span><span class="sxs-lookup"><span data-stu-id="4775b-129">OUTPUTS</span></span>

### <span data-ttu-id="4775b-130">RegulatoryCompliance. PSSecurityRegulatoryComplianceStandard에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="4775b-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="4775b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4775b-131">NOTES</span></span>

## <span data-ttu-id="4775b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4775b-132">RELATED LINKS</span></span>
