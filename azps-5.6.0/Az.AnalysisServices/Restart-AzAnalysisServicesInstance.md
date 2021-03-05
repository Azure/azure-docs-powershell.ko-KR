---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: b0bb5d90fe304d2663671fdc8a2277d2adb18322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975963"
---
# <span data-ttu-id="1ee63-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="1ee63-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="1ee63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ee63-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee63-103">현재 로그온된 환경의 Analysis Services 서버 인스턴스를 Add-AzAnalysisServicesAccount 명령에 따라 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="1ee63-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ee63-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee63-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ee63-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee63-106">Restart-AzAnalysisServicesInstance cmdlet이 Azure Analysis Services 서버의 인스턴스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="1ee63-107">예제</span><span class="sxs-lookup"><span data-stu-id="1ee63-107">EXAMPLES</span></span>

### <span data-ttu-id="1ee63-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ee63-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="1ee63-109">이 명령은 명령에 지정된 환경에서 서버 'testserver'를 다시 Add-AzAnalysisServicesAccount 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="1ee63-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ee63-110">PARAMETERS</span></span>

### <span data-ttu-id="1ee63-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="1ee63-111">-Instance</span></span>
<span data-ttu-id="1ee63-112">다시 시작할 Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="1ee63-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="1ee63-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ee63-113">-PassThru</span></span>
<span data-ttu-id="1ee63-114">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1ee63-115">-확인</span><span class="sxs-lookup"><span data-stu-id="1ee63-115">-Confirm</span></span>
<span data-ttu-id="1ee63-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee63-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee63-117">-WhatIf</span></span>
<span data-ttu-id="1ee63-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ee63-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee63-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee63-120">CommonParameters</span></span>
<span data-ttu-id="1ee63-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee63-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee63-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1ee63-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee63-123">입력</span><span class="sxs-lookup"><span data-stu-id="1ee63-123">INPUTS</span></span>

### <span data-ttu-id="1ee63-124">없음</span><span class="sxs-lookup"><span data-stu-id="1ee63-124">None</span></span>

## <span data-ttu-id="1ee63-125">출력</span><span class="sxs-lookup"><span data-stu-id="1ee63-125">OUTPUTS</span></span>

### <span data-ttu-id="1ee63-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ee63-126">System.Boolean</span></span>

## <span data-ttu-id="1ee63-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ee63-127">NOTES</span></span>
<span data-ttu-id="1ee63-128">별칭: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="1ee63-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="1ee63-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ee63-129">RELATED LINKS</span></span>
