---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 3e4e3b2c2f90420f198d2900d5de0d519ffde81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015547"
---
# <span data-ttu-id="1ffb8-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="1ffb8-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="1ffb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ffb8-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffb8-103">현재 로깅된 환경의 Analysis Services 서버 인스턴스에서 로그를 Add-AzAnalysisServicesAccount 명령</span><span class="sxs-lookup"><span data-stu-id="1ffb8-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="1ffb8-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ffb8-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ffb8-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ffb8-105">DESCRIPTION</span></span>
<span data-ttu-id="1ffb8-106">Export-AzAnalysisServicesInstance cmdlet은 Azure Analysis Services 서버 인스턴스에서 파일로 로그를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ffb8-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="1ffb8-107">예제</span><span class="sxs-lookup"><span data-stu-id="1ffb8-107">EXAMPLES</span></span>

### <span data-ttu-id="1ffb8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ffb8-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="1ffb8-109">이 명령은 Add-AzAnalysisServicesAccount 명령에 지정된 환경에서 서버 'testserver'에서 로그를 내보낸 다음 OutputPath 'C:\path\to\log\testserver.log'에 지정된 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1ffb8-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="1ffb8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ffb8-110">PARAMETERS</span></span>

### <span data-ttu-id="1ffb8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1ffb8-111">-Force</span></span>
<span data-ttu-id="1ffb8-112">묻지 않고 존재하는 경우 파일을 덮어</span><span class="sxs-lookup"><span data-stu-id="1ffb8-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="1ffb8-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="1ffb8-113">-Instance</span></span>
<span data-ttu-id="1ffb8-114">Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="1ffb8-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="1ffb8-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1ffb8-115">-OutputPath</span></span>
<span data-ttu-id="1ffb8-116">로그를 내보낼 파일에 대한 출력 경로</span><span class="sxs-lookup"><span data-stu-id="1ffb8-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="1ffb8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ffb8-117">-PassThru</span></span>
<span data-ttu-id="1ffb8-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1ffb8-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1ffb8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1ffb8-119">-Confirm</span></span>
<span data-ttu-id="1ffb8-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ffb8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ffb8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ffb8-121">-WhatIf</span></span>
<span data-ttu-id="1ffb8-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ffb8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ffb8-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ffb8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ffb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffb8-124">CommonParameters</span></span>
<span data-ttu-id="1ffb8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ffb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffb8-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1ffb8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffb8-127">입력</span><span class="sxs-lookup"><span data-stu-id="1ffb8-127">INPUTS</span></span>

### <span data-ttu-id="1ffb8-128">없음</span><span class="sxs-lookup"><span data-stu-id="1ffb8-128">None</span></span>

## <span data-ttu-id="1ffb8-129">출력</span><span class="sxs-lookup"><span data-stu-id="1ffb8-129">OUTPUTS</span></span>

### <span data-ttu-id="1ffb8-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="1ffb8-130">System.Void</span></span>

## <span data-ttu-id="1ffb8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ffb8-131">NOTES</span></span>
<span data-ttu-id="1ffb8-132">별칭: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="1ffb8-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="1ffb8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ffb8-133">RELATED LINKS</span></span>
