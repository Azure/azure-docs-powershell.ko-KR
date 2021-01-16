---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
ms.openlocfilehash: 019f37fa6b735b506c71a914a6ea59700565fd49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341534"
---
# <span data-ttu-id="8821d-101">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="8821d-101">Get-AzSupportService</span></span>

## <span data-ttu-id="8821d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8821d-102">SYNOPSIS</span></span>
<span data-ttu-id="8821d-103">지원을 사용할 수 있는 서비스를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-103">Get services for which support is available.</span></span> 

## <span data-ttu-id="8821d-104">구문</span><span class="sxs-lookup"><span data-stu-id="8821d-104">SYNTAX</span></span>

### <span data-ttu-id="8821d-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8821d-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportService [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821d-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8821d-106">GetByNameParameterSet</span></span>
```
Get-AzSupportService -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8821d-107">설명</span><span class="sxs-lookup"><span data-stu-id="8821d-107">DESCRIPTION</span></span>
<span data-ttu-id="8821d-108">지원을 사용할 수 있는 Azure 서비스의 현재 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-108">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="8821d-109">각 서비스에는 하나 이상의 Azure 리소스 관리자(ARM) 리소스 종류 정보가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-109">Each service may contain one or more Azure resource manager (ARM) resource type information.</span></span> <span data-ttu-id="8821d-110">리소스 종류(예: 'microsoft.compute/virtualmachines')는 기술 지원 티켓을 만들 때 올바른 제품 및 ARM 리소스를 매핑하는 데 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-110">Resource types (example: 'microsoft.compute/virtualmachines') can be useful to map the right product and ARM resource when creating a technical support ticket.</span></span> <span data-ttu-id="8821d-111">각 Azure 서비스에는 문제 분류라는 자체 범주 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-111">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="8821d-112">Get-AzSupportProblemClassification을 사용하여 서비스에 대한 현재 문제 분류 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-112">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="8821d-113">서비스 및 문제 분류 GUID를 사용하여 New-AzSupportTicket을 사용하여 새 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="8821d-114">항상 프로그래밍으로 얻은 서비스 및 문제 분류 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-114">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="8821d-115">이 연습을 통해 지원 티켓을 만들기 위한 최신 서비스 및 문제 분류 GUID 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-115">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="8821d-116">예제</span><span class="sxs-lookup"><span data-stu-id="8821d-116">EXAMPLES</span></span>

### <span data-ttu-id="8821d-117">예제 1: 지원에 사용할 수 있는 모든 서비스 다운로드</span><span class="sxs-lookup"><span data-stu-id="8821d-117">Example 1: Get all services available for support</span></span>
```powershell
PS C:\> Get-AzSupportService

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
809e8afe-489e-08b0-95f2-08f835a383e8 Advanced Threat Protection - Azure
6859f4e8-4a1d-13e4-f276-6d055007e83d Advanced Threat Protection - Microsoft Defender
94332e54-73b0-b8e3-306e-db3ad13d950b Advanced Threat Protection - O365
26d8424b-0a41-4443-cbc6-0309ea8708d0 Advisor
8f1ddc5f-0c5e-50c7-9810-e01a8d1da925 AKS Engine on Azure Stack
c1840ac9-309f-f235-c0ae-4782f283b698 Alerts and Action Groups
e8fe7c6f-d883-c57f-6576-cf801ca30653 Analysis Services
07651e65-958a-0877-36f3-61bbba85d783 API for FHIR
b4d0e877-0166-0474-9a76-b5be30ba40e4 API Management Service
e14f616b-42c5-4515-3d7c-67935eece51a App Configuration
445c0905-55e2-4f42-d853-ec9e17a5180e App Service Certificates
b7d2f8b7-7d20-cf2f-ddd5-5543ada54bd2 App Service Domains
101732bb-31af-ee61-7c16-d4ad77c86a50 Application Gateway
```

### <span data-ttu-id="8821d-118">예제 2: 지원에 사용할 수 있는 ID로 단일 서비스의 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="8821d-118">Example 2: Get details of a single service by id available for support</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "484e2236-bc6d-b1bb-76d2-7d09278cf9ea"

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
```

## <span data-ttu-id="8821d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8821d-119">PARAMETERS</span></span>

### <span data-ttu-id="8821d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8821d-120">-DefaultProfile</span></span>
<span data-ttu-id="8821d-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8821d-122">-Id</span><span class="sxs-lookup"><span data-stu-id="8821d-122">-Id</span></span>
<span data-ttu-id="8821d-123">서비스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-123">Service id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8821d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8821d-124">CommonParameters</span></span>
<span data-ttu-id="8821d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8821d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8821d-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8821d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8821d-127">입력</span><span class="sxs-lookup"><span data-stu-id="8821d-127">INPUTS</span></span>

### <span data-ttu-id="8821d-128">없음</span><span class="sxs-lookup"><span data-stu-id="8821d-128">None</span></span>

## <span data-ttu-id="8821d-129">출력</span><span class="sxs-lookup"><span data-stu-id="8821d-129">OUTPUTS</span></span>

### <span data-ttu-id="8821d-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="8821d-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="8821d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8821d-131">NOTES</span></span>

## <span data-ttu-id="8821d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8821d-132">RELATED LINKS</span></span>