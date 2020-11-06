---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 9dd8a86d1e98268708d7b0a12448df109ee083f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536879"
---
# <span data-ttu-id="14b52-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="14b52-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="14b52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b52-102">SYNOPSIS</span></span>
<span data-ttu-id="14b52-103">Analysis Services 서버의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b52-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14b52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14b52-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14b52-105">DESCRIPTION</span></span>
<span data-ttu-id="14b52-106">Test-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b52-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="14b52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14b52-107">EXAMPLES</span></span>

### <span data-ttu-id="14b52-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="14b52-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="14b52-109">이 명령은 resourcegroup testserver에 testserver 라는 서버가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b52-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="14b52-110">변수</span><span class="sxs-lookup"><span data-stu-id="14b52-110">PARAMETERS</span></span>

### <span data-ttu-id="14b52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b52-111">-DefaultProfile</span></span>
<span data-ttu-id="14b52-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14b52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b52-113">-이름</span><span class="sxs-lookup"><span data-stu-id="14b52-113">-Name</span></span>
<span data-ttu-id="14b52-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14b52-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b52-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b52-115">-ResourceGroupName</span></span>
<span data-ttu-id="14b52-116">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="14b52-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b52-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b52-117">CommonParameters</span></span>
<span data-ttu-id="14b52-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14b52-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b52-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b52-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b52-120">입력</span><span class="sxs-lookup"><span data-stu-id="14b52-120">INPUTS</span></span>

### <span data-ttu-id="14b52-121">않아야</span><span class="sxs-lookup"><span data-stu-id="14b52-121">None</span></span>
<span data-ttu-id="14b52-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14b52-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14b52-123">출력</span><span class="sxs-lookup"><span data-stu-id="14b52-123">OUTPUTS</span></span>

### <span data-ttu-id="14b52-124">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="14b52-124">System.Boolean</span></span>

## <span data-ttu-id="14b52-125">상속자</span><span class="sxs-lookup"><span data-stu-id="14b52-125">NOTES</span></span>
<span data-ttu-id="14b52-126">별칭: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="14b52-126">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="14b52-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14b52-127">RELATED LINKS</span></span>

[<span data-ttu-id="14b52-128">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="14b52-128">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="14b52-129">제거-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="14b52-129">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
