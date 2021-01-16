---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382439"
---
# <span data-ttu-id="3d0c6-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="3d0c6-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="3d0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="3d0c6-103">게이트웨이로 들어오는/보내기 HTTP 메시지에 대한 진단 설정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="3d0c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d0c6-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d0c6-105">설명</span><span class="sxs-lookup"><span data-stu-id="3d0c6-105">DESCRIPTION</span></span>
<span data-ttu-id="3d0c6-106">**New-AzApiManagementPipelineDiagnosticSetting** cmdlet은 게이트웨이로 들어오는/발신 HTTP 메시지에 대한 진단 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="3d0c6-107">예제</span><span class="sxs-lookup"><span data-stu-id="3d0c6-107">EXAMPLES</span></span>

### <span data-ttu-id="3d0c6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d0c6-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="3d0c6-109">진단 엔터티의 FrontEnd 또는 백 엔드에서 사용할 파이프라인 진단을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="3d0c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d0c6-110">PARAMETERS</span></span>

### <span data-ttu-id="3d0c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d0c6-111">-DefaultProfile</span></span>
<span data-ttu-id="3d0c6-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d0c6-113">-Request</span><span class="sxs-lookup"><span data-stu-id="3d0c6-113">-Request</span></span>
<span data-ttu-id="3d0c6-114">요청에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="3d0c6-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d0c6-116">-Response</span><span class="sxs-lookup"><span data-stu-id="3d0c6-116">-Response</span></span>
<span data-ttu-id="3d0c6-117">응답에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="3d0c6-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d0c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0c6-119">CommonParameters</span></span>
<span data-ttu-id="3d0c6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0c6-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0c6-122">입력</span><span class="sxs-lookup"><span data-stu-id="3d0c6-122">INPUTS</span></span>

### <span data-ttu-id="3d0c6-123">없음</span><span class="sxs-lookup"><span data-stu-id="3d0c6-123">None</span></span>

## <span data-ttu-id="3d0c6-124">출력</span><span class="sxs-lookup"><span data-stu-id="3d0c6-124">OUTPUTS</span></span>

### <span data-ttu-id="3d0c6-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="3d0c6-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="3d0c6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d0c6-126">NOTES</span></span>

## <span data-ttu-id="3d0c6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d0c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="3d0c6-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3d0c6-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="3d0c6-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3d0c6-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="3d0c6-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3d0c6-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="3d0c6-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3d0c6-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

