---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: f2d9c12cb3795d23144fa5296cba992a25383819
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698034"
---
# <span data-ttu-id="0fc3b-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0fc3b-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="0fc3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc3b-103">들어오는/나가는 HTTP 메시지에 대 한 진단 설정을 게이트웨이에 대해 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="0fc3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fc3b-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fc3b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0fc3b-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc3b-106">Cmdlet **AzApiManagementPipelineDiagnosticSetting** 는 게이트웨이로 들어오는/나가는 HTTP 메시지에 대 한 진단 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="0fc3b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0fc3b-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc3b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0fc3b-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="0fc3b-109">진단 엔터티에서 프런트 엔드 또는 백 엔드에 사용할 파이프라인 진단을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="0fc3b-110">변수</span><span class="sxs-lookup"><span data-stu-id="0fc3b-110">PARAMETERS</span></span>

### <span data-ttu-id="0fc3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc3b-111">-DefaultProfile</span></span>
<span data-ttu-id="0fc3b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc3b-113">-요청</span><span class="sxs-lookup"><span data-stu-id="0fc3b-113">-Request</span></span>
<span data-ttu-id="0fc3b-114">요청에 대 한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="0fc3b-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="0fc3b-116">-응답</span><span class="sxs-lookup"><span data-stu-id="0fc3b-116">-Response</span></span>
<span data-ttu-id="0fc3b-117">응답에 대 한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="0fc3b-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="0fc3b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc3b-119">CommonParameters</span></span>
<span data-ttu-id="0fc3b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc3b-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc3b-122">입력</span><span class="sxs-lookup"><span data-stu-id="0fc3b-122">INPUTS</span></span>

### <span data-ttu-id="0fc3b-123">않아야</span><span class="sxs-lookup"><span data-stu-id="0fc3b-123">None</span></span>

## <span data-ttu-id="0fc3b-124">출력</span><span class="sxs-lookup"><span data-stu-id="0fc3b-124">OUTPUTS</span></span>

### <span data-ttu-id="0fc3b-125">ApiManagement. ServiceManagement. \ PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0fc3b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="0fc3b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="0fc3b-126">NOTES</span></span>

## <span data-ttu-id="0fc3b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fc3b-127">RELATED LINKS</span></span>

[<span data-ttu-id="0fc3b-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0fc3b-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0fc3b-129">제거-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0fc3b-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0fc3b-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0fc3b-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="0fc3b-131">새로운 AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0fc3b-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


