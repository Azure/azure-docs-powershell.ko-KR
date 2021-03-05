---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: e68449a84bb64454291434bded40ed2e494fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979051"
---
# <span data-ttu-id="4b993-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4b993-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="4b993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b993-102">SYNOPSIS</span></span>
<span data-ttu-id="4b993-103">게이트웨이에 들어오는/들어오는 HTTP 메시지에 대한 진단 설정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="4b993-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b993-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b993-105">설명</span><span class="sxs-lookup"><span data-stu-id="4b993-105">DESCRIPTION</span></span>
<span data-ttu-id="4b993-106">cmdlet **New-AzApiManagementPipelineDiagnosticSetting은** 게이트웨이에 들어오는/발신 HTTP 메시지에 대한 진단 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="4b993-107">예제</span><span class="sxs-lookup"><span data-stu-id="4b993-107">EXAMPLES</span></span>

### <span data-ttu-id="4b993-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b993-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="4b993-109">진단 엔터티의 FrontEnd 또는 Backend에서 사용할 파이프라인 진단을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="4b993-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b993-110">PARAMETERS</span></span>

### <span data-ttu-id="4b993-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b993-111">-DefaultProfile</span></span>
<span data-ttu-id="4b993-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b993-113">-Request</span><span class="sxs-lookup"><span data-stu-id="4b993-113">-Request</span></span>
<span data-ttu-id="4b993-114">요청에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="4b993-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b993-116">-Response</span><span class="sxs-lookup"><span data-stu-id="4b993-116">-Response</span></span>
<span data-ttu-id="4b993-117">응답에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="4b993-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b993-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b993-119">CommonParameters</span></span>
<span data-ttu-id="4b993-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b993-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b993-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b993-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b993-122">입력</span><span class="sxs-lookup"><span data-stu-id="4b993-122">INPUTS</span></span>

### <span data-ttu-id="4b993-123">없음</span><span class="sxs-lookup"><span data-stu-id="4b993-123">None</span></span>

## <span data-ttu-id="4b993-124">출력</span><span class="sxs-lookup"><span data-stu-id="4b993-124">OUTPUTS</span></span>

### <span data-ttu-id="4b993-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4b993-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="4b993-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b993-126">NOTES</span></span>

## <span data-ttu-id="4b993-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b993-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b993-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4b993-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4b993-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4b993-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4b993-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4b993-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4b993-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4b993-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


