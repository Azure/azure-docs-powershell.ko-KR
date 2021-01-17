---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345621"
---
# <span data-ttu-id="3ee06-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3ee06-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="3ee06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee06-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee06-103">Analysis Services 서버 인스턴스의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee06-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="3ee06-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ee06-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee06-105">설명</span><span class="sxs-lookup"><span data-stu-id="3ee06-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee06-106">Test-AzAnalysisServicesServer cmdlet은 Analysis Services 서버 인스턴스의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee06-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="3ee06-107">예제</span><span class="sxs-lookup"><span data-stu-id="3ee06-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee06-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ee06-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="3ee06-109">이 명령은 리소스 그룹 테스트 그룹에서 테스트 서버라는 서버가 있는 경우 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee06-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="3ee06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ee06-110">PARAMETERS</span></span>

### <span data-ttu-id="3ee06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee06-111">-DefaultProfile</span></span>
<span data-ttu-id="3ee06-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ee06-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3ee06-113">-Name</span></span>
<span data-ttu-id="3ee06-114">Analysis Services 서버의 이름</span><span class="sxs-lookup"><span data-stu-id="3ee06-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="3ee06-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee06-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ee06-116">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="3ee06-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="3ee06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee06-117">CommonParameters</span></span>
<span data-ttu-id="3ee06-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee06-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3ee06-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee06-120">입력</span><span class="sxs-lookup"><span data-stu-id="3ee06-120">INPUTS</span></span>

### <span data-ttu-id="3ee06-121">System.String</span><span class="sxs-lookup"><span data-stu-id="3ee06-121">System.String</span></span>

## <span data-ttu-id="3ee06-122">출력</span><span class="sxs-lookup"><span data-stu-id="3ee06-122">OUTPUTS</span></span>

### <span data-ttu-id="3ee06-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ee06-123">System.Boolean</span></span>

## <span data-ttu-id="3ee06-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ee06-124">NOTES</span></span>
<span data-ttu-id="3ee06-125">별칭: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="3ee06-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="3ee06-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ee06-126">RELATED LINKS</span></span>

[<span data-ttu-id="3ee06-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3ee06-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="3ee06-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3ee06-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
