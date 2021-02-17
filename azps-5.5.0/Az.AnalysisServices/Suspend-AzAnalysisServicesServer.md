---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192572"
---
# <span data-ttu-id="e9cb3-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e9cb3-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="e9cb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="e9cb3-103">Analysis Services 서버의 인스턴스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="e9cb3-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9cb3-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9cb3-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="e9cb3-106">Suspend-AzAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="e9cb3-107">예제</span><span class="sxs-lookup"><span data-stu-id="e9cb3-107">EXAMPLES</span></span>

### <span data-ttu-id="e9cb3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9cb3-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="e9cb3-109">이 명령은 리소스 그룹 테스트 그룹에서 testserver라는 활성 서버를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="e9cb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9cb3-110">PARAMETERS</span></span>

### <span data-ttu-id="e9cb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9cb3-111">-DefaultProfile</span></span>
<span data-ttu-id="e9cb3-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9cb3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e9cb3-113">-Name</span></span>
<span data-ttu-id="e9cb3-114">Analysis Services 서버의 이름</span><span class="sxs-lookup"><span data-stu-id="e9cb3-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="e9cb3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9cb3-115">-PassThru</span></span>
<span data-ttu-id="e9cb3-116">작업이 성공적으로 완료되면 삭제된 서버 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="e9cb3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9cb3-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9cb3-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e9cb3-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="e9cb3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9cb3-119">-Confirm</span></span>
<span data-ttu-id="e9cb3-120">사용자에게 작업을 수행할지 여부를 확인하도록 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e9cb3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9cb3-121">-WhatIf</span></span>
<span data-ttu-id="e9cb3-122">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e9cb3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9cb3-123">CommonParameters</span></span>
<span data-ttu-id="e9cb3-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9cb3-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9cb3-126">입력</span><span class="sxs-lookup"><span data-stu-id="e9cb3-126">INPUTS</span></span>

### <span data-ttu-id="e9cb3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e9cb3-127">System.String</span></span>

## <span data-ttu-id="e9cb3-128">출력</span><span class="sxs-lookup"><span data-stu-id="e9cb3-128">OUTPUTS</span></span>

### <span data-ttu-id="e9cb3-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e9cb3-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="e9cb3-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9cb3-130">NOTES</span></span>
<span data-ttu-id="e9cb3-131">별칭: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="e9cb3-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="e9cb3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9cb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="e9cb3-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e9cb3-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="e9cb3-134">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e9cb3-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

