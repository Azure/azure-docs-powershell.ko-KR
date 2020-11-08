---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043947"
---
# <span data-ttu-id="19718-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="19718-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="19718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19718-102">SYNOPSIS</span></span>
<span data-ttu-id="19718-103">Analysis Services 서버의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19718-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="19718-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19718-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19718-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19718-105">DESCRIPTION</span></span>
<span data-ttu-id="19718-106">Test-AzAnalysisServicesServer cmdlet은 Analysis Services 서버 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19718-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="19718-107">예제의</span><span class="sxs-lookup"><span data-stu-id="19718-107">EXAMPLES</span></span>

### <span data-ttu-id="19718-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="19718-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="19718-109">이 명령은 resourcegroup testserver에 testserver 라는 서버가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19718-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="19718-110">변수</span><span class="sxs-lookup"><span data-stu-id="19718-110">PARAMETERS</span></span>

### <span data-ttu-id="19718-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19718-111">-DefaultProfile</span></span>
<span data-ttu-id="19718-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19718-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19718-113">-이름</span><span class="sxs-lookup"><span data-stu-id="19718-113">-Name</span></span>
<span data-ttu-id="19718-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19718-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="19718-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19718-115">-ResourceGroupName</span></span>
<span data-ttu-id="19718-116">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="19718-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="19718-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19718-117">CommonParameters</span></span>
<span data-ttu-id="19718-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19718-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19718-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19718-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19718-120">입력</span><span class="sxs-lookup"><span data-stu-id="19718-120">INPUTS</span></span>

### <span data-ttu-id="19718-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19718-121">System.String</span></span>

## <span data-ttu-id="19718-122">출력</span><span class="sxs-lookup"><span data-stu-id="19718-122">OUTPUTS</span></span>

### <span data-ttu-id="19718-123">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="19718-123">System.Boolean</span></span>

## <span data-ttu-id="19718-124">상속자</span><span class="sxs-lookup"><span data-stu-id="19718-124">NOTES</span></span>
<span data-ttu-id="19718-125">별칭: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="19718-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="19718-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19718-126">RELATED LINKS</span></span>

[<span data-ttu-id="19718-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="19718-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="19718-128">제거-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="19718-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
