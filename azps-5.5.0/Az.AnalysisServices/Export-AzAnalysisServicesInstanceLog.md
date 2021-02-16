---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199769"
---
# <span data-ttu-id="59ee7-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="59ee7-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="59ee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="59ee7-103">현재 로그인한 환경의 Analysis Services 서버 인스턴스에서 로그를 Add-AzAnalysisServicesAccount 명령에 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="59ee7-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="59ee7-104">구문</span><span class="sxs-lookup"><span data-stu-id="59ee7-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59ee7-105">설명</span><span class="sxs-lookup"><span data-stu-id="59ee7-105">DESCRIPTION</span></span>
<span data-ttu-id="59ee7-106">Export-AzAnalysisServicesInstance cmdlet은 Azure Analysis Services 서버의 인스턴스에서 파일로 로그를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59ee7-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="59ee7-107">예제</span><span class="sxs-lookup"><span data-stu-id="59ee7-107">EXAMPLES</span></span>

### <span data-ttu-id="59ee7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="59ee7-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="59ee7-109">이 명령은 Add-AzAnalysisServicesAccount 명령에 지정된 환경의 서버 'testserver'에서 로그를 내보내고 OutputPath 'C:\path\to\log\testserver.log'에 지정된 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="59ee7-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="59ee7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59ee7-110">PARAMETERS</span></span>

### <span data-ttu-id="59ee7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="59ee7-111">-Force</span></span>
<span data-ttu-id="59ee7-112">요청하지 않고 있는 경우 파일을 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="59ee7-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="59ee7-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="59ee7-113">-Instance</span></span>
<span data-ttu-id="59ee7-114">Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="59ee7-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59ee7-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="59ee7-115">-OutputPath</span></span>
<span data-ttu-id="59ee7-116">로그를 내보낼 파일에 대한 출력 경로</span><span class="sxs-lookup"><span data-stu-id="59ee7-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ee7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59ee7-117">-PassThru</span></span>
<span data-ttu-id="59ee7-118">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="59ee7-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="59ee7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59ee7-119">-Confirm</span></span>
<span data-ttu-id="59ee7-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59ee7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59ee7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59ee7-121">-WhatIf</span></span>
<span data-ttu-id="59ee7-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="59ee7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59ee7-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59ee7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59ee7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ee7-124">CommonParameters</span></span>
<span data-ttu-id="59ee7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59ee7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ee7-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59ee7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ee7-127">입력</span><span class="sxs-lookup"><span data-stu-id="59ee7-127">INPUTS</span></span>

### <span data-ttu-id="59ee7-128">없음</span><span class="sxs-lookup"><span data-stu-id="59ee7-128">None</span></span>

## <span data-ttu-id="59ee7-129">출력</span><span class="sxs-lookup"><span data-stu-id="59ee7-129">OUTPUTS</span></span>

### <span data-ttu-id="59ee7-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="59ee7-130">System.Void</span></span>

## <span data-ttu-id="59ee7-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59ee7-131">NOTES</span></span>
<span data-ttu-id="59ee7-132">별칭: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="59ee7-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="59ee7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59ee7-133">RELATED LINKS</span></span>
