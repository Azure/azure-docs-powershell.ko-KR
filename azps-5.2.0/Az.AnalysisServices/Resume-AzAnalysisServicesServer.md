---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338805"
---
# <span data-ttu-id="f2984-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f2984-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="f2984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2984-102">SYNOPSIS</span></span>
<span data-ttu-id="f2984-103">Analysis Services 서버의 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f2984-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2984-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2984-105">설명</span><span class="sxs-lookup"><span data-stu-id="f2984-105">DESCRIPTION</span></span>
<span data-ttu-id="f2984-106">Resume-AzAnalysisServicesServer cmdlet이 Analysis Services 서버의 인스턴스를 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f2984-107">예제</span><span class="sxs-lookup"><span data-stu-id="f2984-107">EXAMPLES</span></span>

### <span data-ttu-id="f2984-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2984-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="f2984-109">이 명령은 리소스 그룹 테스트 그룹에서 테스트 서버라는 일시 중지된 서버를 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="f2984-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2984-110">PARAMETERS</span></span>

### <span data-ttu-id="f2984-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2984-111">-DefaultProfile</span></span>
<span data-ttu-id="f2984-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2984-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f2984-113">-Name</span></span>
<span data-ttu-id="f2984-114">Analysis Services 서버의 이름</span><span class="sxs-lookup"><span data-stu-id="f2984-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2984-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2984-115">-PassThru</span></span>
<span data-ttu-id="f2984-116">작업이 성공적으로 완료되면 삭제된 서버 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2984-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2984-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2984-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="f2984-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2984-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2984-119">-Confirm</span></span>
<span data-ttu-id="f2984-120">사용자에게 작업을 수행할지 여부를 확인하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2984-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2984-121">-WhatIf</span></span>
<span data-ttu-id="f2984-122">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2984-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2984-123">CommonParameters</span></span>
<span data-ttu-id="f2984-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2984-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2984-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f2984-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2984-126">입력</span><span class="sxs-lookup"><span data-stu-id="f2984-126">INPUTS</span></span>

### <span data-ttu-id="f2984-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f2984-127">System.String</span></span>

## <span data-ttu-id="f2984-128">출력</span><span class="sxs-lookup"><span data-stu-id="f2984-128">OUTPUTS</span></span>

### <span data-ttu-id="f2984-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f2984-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f2984-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2984-130">NOTES</span></span>
<span data-ttu-id="f2984-131">별칭: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="f2984-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="f2984-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2984-132">RELATED LINKS</span></span>

[<span data-ttu-id="f2984-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f2984-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="f2984-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f2984-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
