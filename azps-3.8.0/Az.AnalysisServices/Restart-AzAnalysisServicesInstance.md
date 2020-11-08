---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042045"
---
# <span data-ttu-id="0bf54-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="0bf54-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="0bf54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf54-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf54-103">Add-AzAnalysisServicesAccount 명령에 지정 된 대로 현재 로그인 한 환경에서 Analysis Services 서버 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="0bf54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0bf54-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bf54-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0bf54-105">DESCRIPTION</span></span>
<span data-ttu-id="0bf54-106">Restart-AzAnalysisServicesInstance cmdlet이 Azure Analysis Services 서버의 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="0bf54-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0bf54-107">EXAMPLES</span></span>

### <span data-ttu-id="0bf54-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0bf54-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="0bf54-109">이 명령을 실행 하면 Add-AzAnalysisServicesAccount 명령에 지정 된 환경에서 서버 ' testserver '가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="0bf54-110">변수</span><span class="sxs-lookup"><span data-stu-id="0bf54-110">PARAMETERS</span></span>

### <span data-ttu-id="0bf54-111">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="0bf54-111">-Instance</span></span>
<span data-ttu-id="0bf54-112">다시 시작할 Analysis Services 서버 인스턴스의 이름</span><span class="sxs-lookup"><span data-stu-id="0bf54-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="0bf54-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bf54-113">-PassThru</span></span>
<span data-ttu-id="0bf54-114">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0bf54-115">-확인</span><span class="sxs-lookup"><span data-stu-id="0bf54-115">-Confirm</span></span>
<span data-ttu-id="0bf54-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bf54-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bf54-117">-WhatIf</span></span>
<span data-ttu-id="0bf54-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bf54-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bf54-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf54-120">CommonParameters</span></span>
<span data-ttu-id="0bf54-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf54-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf54-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bf54-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf54-123">입력</span><span class="sxs-lookup"><span data-stu-id="0bf54-123">INPUTS</span></span>

### <span data-ttu-id="0bf54-124">않아야</span><span class="sxs-lookup"><span data-stu-id="0bf54-124">None</span></span>

## <span data-ttu-id="0bf54-125">출력</span><span class="sxs-lookup"><span data-stu-id="0bf54-125">OUTPUTS</span></span>

### <span data-ttu-id="0bf54-126">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0bf54-126">System.Boolean</span></span>

## <span data-ttu-id="0bf54-127">상속자</span><span class="sxs-lookup"><span data-stu-id="0bf54-127">NOTES</span></span>
<span data-ttu-id="0bf54-128">별칭: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="0bf54-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="0bf54-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bf54-129">RELATED LINKS</span></span>
