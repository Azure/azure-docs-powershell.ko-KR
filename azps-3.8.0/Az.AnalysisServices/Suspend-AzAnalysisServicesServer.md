---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041963"
---
# <span data-ttu-id="5d869-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5d869-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="5d869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d869-102">SYNOPSIS</span></span>
<span data-ttu-id="5d869-103">Analysis Services 서버 인스턴스 일시 중단</span><span class="sxs-lookup"><span data-stu-id="5d869-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="5d869-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d869-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d869-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d869-105">DESCRIPTION</span></span>
<span data-ttu-id="5d869-106">Suspend-AzAnalysisServicesServer cmdlet이 Analysis Services 서버 인스턴스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d869-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="5d869-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5d869-107">EXAMPLES</span></span>

### <span data-ttu-id="5d869-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d869-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="5d869-109">이 명령은 resourcegroup testserver에서 testserver 라는 활성 서버를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d869-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="5d869-110">변수</span><span class="sxs-lookup"><span data-stu-id="5d869-110">PARAMETERS</span></span>

### <span data-ttu-id="5d869-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d869-111">-DefaultProfile</span></span>
<span data-ttu-id="5d869-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d869-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d869-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5d869-113">-Name</span></span>
<span data-ttu-id="5d869-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d869-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="5d869-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d869-115">-PassThru</span></span>
<span data-ttu-id="5d869-116">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d869-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="5d869-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d869-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d869-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5d869-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="5d869-119">-확인</span><span class="sxs-lookup"><span data-stu-id="5d869-119">-Confirm</span></span>
<span data-ttu-id="5d869-120">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="5d869-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="5d869-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d869-121">-WhatIf</span></span>
<span data-ttu-id="5d869-122">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d869-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="5d869-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d869-123">CommonParameters</span></span>
<span data-ttu-id="5d869-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d869-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d869-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d869-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d869-126">입력</span><span class="sxs-lookup"><span data-stu-id="5d869-126">INPUTS</span></span>

### <span data-ttu-id="5d869-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d869-127">System.String</span></span>

## <span data-ttu-id="5d869-128">출력</span><span class="sxs-lookup"><span data-stu-id="5d869-128">OUTPUTS</span></span>

### <span data-ttu-id="5d869-129">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="5d869-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="5d869-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5d869-130">NOTES</span></span>
<span data-ttu-id="5d869-131">별칭: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="5d869-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="5d869-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d869-132">RELATED LINKS</span></span>

[<span data-ttu-id="5d869-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5d869-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="5d869-134">이력서-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5d869-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

