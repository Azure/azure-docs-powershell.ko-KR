---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528709"
---
# <span data-ttu-id="7e4a1-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="7e4a1-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="7e4a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4a1-103">Add-AzureAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경의 Analysis Services 서버 인스턴스에서 로그를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e4a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e4a1-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e4a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e4a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e4a1-106">Export-AzureAnalysisServicesInstance cmdlet은 Azure Analysis Services 서버 인스턴스에서 로그를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="7e4a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7e4a1-107">EXAMPLES</span></span>

### <span data-ttu-id="7e4a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e4a1-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="7e4a1-109">이 명령은 Add-AzureAnalysisServicesAccount 명령에 지정 된 환경의 ' testserver ' 서버에서 로그를 내보내고 OutputPath ' C:\path\to\log\testserver.log '에 지정 된 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="7e4a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="7e4a1-110">PARAMETERS</span></span>

### <span data-ttu-id="7e4a1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7e4a1-111">-Force</span></span>
<span data-ttu-id="7e4a1-112">묻지 않고 파일이 있는 경우 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="7e4a1-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="7e4a1-113">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="7e4a1-113">-Instance</span></span>
<span data-ttu-id="7e4a1-114">Analysis Services 서버 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="7e4a1-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="7e4a1-115">-OutputPath</span></span>
<span data-ttu-id="7e4a1-116">내보낼 파일의 출력 경로 로그</span><span class="sxs-lookup"><span data-stu-id="7e4a1-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="7e4a1-117">-확인</span><span class="sxs-lookup"><span data-stu-id="7e4a1-117">-Confirm</span></span>
<span data-ttu-id="7e4a1-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4a1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4a1-119">-WhatIf</span></span>
<span data-ttu-id="7e4a1-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e4a1-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4a1-122">CommonParameters</span></span>
<span data-ttu-id="7e4a1-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4a1-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e4a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4a1-125">입력</span><span class="sxs-lookup"><span data-stu-id="7e4a1-125">INPUTS</span></span>

### <span data-ttu-id="7e4a1-126">않아야</span><span class="sxs-lookup"><span data-stu-id="7e4a1-126">None</span></span>

## <span data-ttu-id="7e4a1-127">출력</span><span class="sxs-lookup"><span data-stu-id="7e4a1-127">OUTPUTS</span></span>

### <span data-ttu-id="7e4a1-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="7e4a1-128">System.Void</span></span>

## <span data-ttu-id="7e4a1-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7e4a1-129">NOTES</span></span>
<span data-ttu-id="7e4a1-130">별칭: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="7e4a1-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="7e4a1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e4a1-131">RELATED LINKS</span></span>
