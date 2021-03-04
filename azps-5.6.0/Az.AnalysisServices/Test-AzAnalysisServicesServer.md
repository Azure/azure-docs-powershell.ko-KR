---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: cb6680276359fddcf9a98cde3e90cb44185c4e85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959211"
---
# <span data-ttu-id="4fe4b-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4fe4b-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="4fe4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe4b-103">Analysis Services 서버 인스턴스의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe4b-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="4fe4b-104">구문</span><span class="sxs-lookup"><span data-stu-id="4fe4b-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fe4b-105">설명</span><span class="sxs-lookup"><span data-stu-id="4fe4b-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe4b-106">Test-AzAnalysisServicesServer cmdlet은 Analysis Services 서버 인스턴스의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe4b-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="4fe4b-107">예제</span><span class="sxs-lookup"><span data-stu-id="4fe4b-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe4b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4fe4b-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="4fe4b-109">이 명령은 리소스 그룹 테스트 그룹에 testserver라는 서버가 있는 경우 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe4b-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4fe4b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4fe4b-110">PARAMETERS</span></span>

### <span data-ttu-id="4fe4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe4b-111">-DefaultProfile</span></span>
<span data-ttu-id="4fe4b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe4b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fe4b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4fe4b-113">-Name</span></span>
<span data-ttu-id="4fe4b-114">Analysis Services 서버 이름</span><span class="sxs-lookup"><span data-stu-id="4fe4b-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4fe4b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe4b-115">-ResourceGroupName</span></span>
<span data-ttu-id="4fe4b-116">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="4fe4b-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="4fe4b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe4b-117">CommonParameters</span></span>
<span data-ttu-id="4fe4b-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe4b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe4b-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fe4b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe4b-120">입력</span><span class="sxs-lookup"><span data-stu-id="4fe4b-120">INPUTS</span></span>

### <span data-ttu-id="4fe4b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4fe4b-121">System.String</span></span>

## <span data-ttu-id="4fe4b-122">출력</span><span class="sxs-lookup"><span data-stu-id="4fe4b-122">OUTPUTS</span></span>

### <span data-ttu-id="4fe4b-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fe4b-123">System.Boolean</span></span>

## <span data-ttu-id="4fe4b-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4fe4b-124">NOTES</span></span>
<span data-ttu-id="4fe4b-125">별칭: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="4fe4b-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="4fe4b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fe4b-126">RELATED LINKS</span></span>

[<span data-ttu-id="4fe4b-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4fe4b-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="4fe4b-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4fe4b-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
