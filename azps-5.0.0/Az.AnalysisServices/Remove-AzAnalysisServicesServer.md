---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216481"
---
# <span data-ttu-id="230d3-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="230d3-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="230d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="230d3-102">SYNOPSIS</span></span>
<span data-ttu-id="230d3-103">Analysis Services 서버 인스턴스 삭제</span><span class="sxs-lookup"><span data-stu-id="230d3-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="230d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="230d3-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="230d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="230d3-105">DESCRIPTION</span></span>
<span data-ttu-id="230d3-106">Remove-AzAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="230d3-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="230d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="230d3-107">EXAMPLES</span></span>

### <span data-ttu-id="230d3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="230d3-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="230d3-109">이 명령은 resourcegroup testserver에서 testserver 라는 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="230d3-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="230d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="230d3-110">PARAMETERS</span></span>

### <span data-ttu-id="230d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230d3-111">-DefaultProfile</span></span>
<span data-ttu-id="230d3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="230d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="230d3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="230d3-113">-Name</span></span>
<span data-ttu-id="230d3-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="230d3-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="230d3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="230d3-115">-PassThru</span></span>
<span data-ttu-id="230d3-116">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="230d3-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="230d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="230d3-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="230d3-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="230d3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="230d3-119">-Confirm</span></span>
<span data-ttu-id="230d3-120">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="230d3-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="230d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="230d3-121">-WhatIf</span></span>
<span data-ttu-id="230d3-122">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="230d3-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="230d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230d3-123">CommonParameters</span></span>
<span data-ttu-id="230d3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="230d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230d3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="230d3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230d3-126">입력</span><span class="sxs-lookup"><span data-stu-id="230d3-126">INPUTS</span></span>

### <span data-ttu-id="230d3-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="230d3-127">System.String</span></span>

## <span data-ttu-id="230d3-128">출력</span><span class="sxs-lookup"><span data-stu-id="230d3-128">OUTPUTS</span></span>

### <span data-ttu-id="230d3-129">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="230d3-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="230d3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="230d3-130">NOTES</span></span>
<span data-ttu-id="230d3-131">별칭: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="230d3-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="230d3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="230d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="230d3-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="230d3-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="230d3-134">새로운 AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="230d3-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
