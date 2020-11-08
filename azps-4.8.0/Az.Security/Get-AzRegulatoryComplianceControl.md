---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212157"
---
# <span data-ttu-id="edc99-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="edc99-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="edc99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edc99-102">SYNOPSIS</span></span>
<span data-ttu-id="edc99-103">규제 준수 제어를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="edc99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="edc99-104">SYNTAX</span></span>

### <span data-ttu-id="edc99-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="edc99-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edc99-106">리소스</span><span class="sxs-lookup"><span data-stu-id="edc99-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edc99-107">설명은</span><span class="sxs-lookup"><span data-stu-id="edc99-107">DESCRIPTION</span></span>
<span data-ttu-id="edc99-108">Spcific 컨트롤 세부 정보를 가져오거나 특정 규제 준수 표준 아래의 모든 컨트롤을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="edc99-109">예제의</span><span class="sxs-lookup"><span data-stu-id="edc99-109">EXAMPLES</span></span>

### <span data-ttu-id="edc99-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="edc99-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="edc99-111">특정 규제 표준에서 모든 컨트롤을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="edc99-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="edc99-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="edc99-113">컨트롤 id에 따라 특정 컨트롤 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="edc99-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="edc99-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="edc99-115">리소스 id에 따라 특정 컨트롤 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="edc99-116">변수</span><span class="sxs-lookup"><span data-stu-id="edc99-116">PARAMETERS</span></span>

### <span data-ttu-id="edc99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc99-117">-DefaultProfile</span></span>
<span data-ttu-id="edc99-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc99-119">-이름</span><span class="sxs-lookup"><span data-stu-id="edc99-119">-Name</span></span>
<span data-ttu-id="edc99-120">컨트롤 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-120">Control Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc99-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edc99-121">-ResourceId</span></span>
<span data-ttu-id="edc99-122">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="edc99-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="edc99-123">-StandardName</span></span>
<span data-ttu-id="edc99-124">표준 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-124">Standard Name.</span></span>

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

### <span data-ttu-id="edc99-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc99-125">CommonParameters</span></span>
<span data-ttu-id="edc99-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="edc99-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc99-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="edc99-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc99-128">입력</span><span class="sxs-lookup"><span data-stu-id="edc99-128">INPUTS</span></span>

### <span data-ttu-id="edc99-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="edc99-129">System.String</span></span>

## <span data-ttu-id="edc99-130">출력</span><span class="sxs-lookup"><span data-stu-id="edc99-130">OUTPUTS</span></span>

### <span data-ttu-id="edc99-131">RegulatoryCompliance. PSSecurityRegulatoryComplianceControl에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="edc99-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="edc99-132">상속자</span><span class="sxs-lookup"><span data-stu-id="edc99-132">NOTES</span></span>

## <span data-ttu-id="edc99-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edc99-133">RELATED LINKS</span></span>
