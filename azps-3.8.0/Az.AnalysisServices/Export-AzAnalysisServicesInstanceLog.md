---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034647"
---
# <span data-ttu-id="b8150-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="b8150-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="b8150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8150-102">SYNOPSIS</span></span>
<span data-ttu-id="b8150-103">Add-AzAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경의 Analysis Services 서버 인스턴스에서 로그를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="b8150-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8150-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8150-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8150-105">DESCRIPTION</span></span>
<span data-ttu-id="b8150-106">Export-AzAnalysisServicesInstance cmdlet은 Azure Analysis Services 서버 인스턴스에서 로그를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="b8150-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8150-107">EXAMPLES</span></span>

### <span data-ttu-id="b8150-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8150-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="b8150-109">이 명령은 Add-AzAnalysisServicesAccount 명령에 지정 된 환경의 ' testserver ' 서버에서 로그를 내보내고 OutputPath ' C:\path\to\log\testserver.log '에 지정 된 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="b8150-110">변수</span><span class="sxs-lookup"><span data-stu-id="b8150-110">PARAMETERS</span></span>

### <span data-ttu-id="b8150-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b8150-111">-Force</span></span>
<span data-ttu-id="b8150-112">묻지 않고 파일이 있는 경우 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="b8150-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="b8150-113">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="b8150-113">-Instance</span></span>
<span data-ttu-id="b8150-114">Analysis Services 서버 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="b8150-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b8150-115">-OutputPath</span></span>
<span data-ttu-id="b8150-116">내보낼 파일의 출력 경로 로그</span><span class="sxs-lookup"><span data-stu-id="b8150-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="b8150-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8150-117">-PassThru</span></span>
<span data-ttu-id="b8150-118">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="b8150-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b8150-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b8150-119">-Confirm</span></span>
<span data-ttu-id="b8150-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8150-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8150-121">-WhatIf</span></span>
<span data-ttu-id="b8150-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8150-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8150-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8150-124">CommonParameters</span></span>
<span data-ttu-id="b8150-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8150-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8150-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8150-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8150-127">입력</span><span class="sxs-lookup"><span data-stu-id="b8150-127">INPUTS</span></span>

### <span data-ttu-id="b8150-128">않아야</span><span class="sxs-lookup"><span data-stu-id="b8150-128">None</span></span>

## <span data-ttu-id="b8150-129">출력</span><span class="sxs-lookup"><span data-stu-id="b8150-129">OUTPUTS</span></span>

### <span data-ttu-id="b8150-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="b8150-130">System.Void</span></span>

## <span data-ttu-id="b8150-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b8150-131">NOTES</span></span>
<span data-ttu-id="b8150-132">별칭: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="b8150-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="b8150-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8150-133">RELATED LINKS</span></span>
