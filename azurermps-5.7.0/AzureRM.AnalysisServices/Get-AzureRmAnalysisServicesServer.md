---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f67c22b483b561af8ffcf2ede9bc1e489379c0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703293"
---
# <span data-ttu-id="b1319-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b1319-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="b1319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1319-102">SYNOPSIS</span></span>
<span data-ttu-id="b1319-103">Analysis Services 서버에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1319-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1319-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1319-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1319-105">DESCRIPTION</span></span>
<span data-ttu-id="b1319-106">Get-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="b1319-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b1319-107">EXAMPLES</span></span>

### <span data-ttu-id="b1319-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1319-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="b1319-109">이 명령은 ResourceGroup03 이라는 리소스 그룹의 모든 Azure Analysis Services 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="b1319-110">예제 2: 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1319-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="b1319-111">이 명령은 ResourceGroup03 이라는 리소스 그룹에서 testserver 라는 Azure Analysis Services 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="b1319-112">변수</span><span class="sxs-lookup"><span data-stu-id="b1319-112">PARAMETERS</span></span>

### <span data-ttu-id="b1319-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1319-113">-DefaultProfile</span></span>
<span data-ttu-id="b1319-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1319-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b1319-115">-Name</span></span>
<span data-ttu-id="b1319-116">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b1319-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1319-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1319-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b1319-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1319-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1319-119">CommonParameters</span></span>
<span data-ttu-id="b1319-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1319-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1319-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1319-122">입력</span><span class="sxs-lookup"><span data-stu-id="b1319-122">INPUTS</span></span>

### <span data-ttu-id="b1319-123">않아야</span><span class="sxs-lookup"><span data-stu-id="b1319-123">None</span></span>
<span data-ttu-id="b1319-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1319-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1319-125">출력</span><span class="sxs-lookup"><span data-stu-id="b1319-125">OUTPUTS</span></span>

### <span data-ttu-id="b1319-126">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="b1319-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="b1319-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b1319-127">NOTES</span></span>
<span data-ttu-id="b1319-128">별칭: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="b1319-128">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="b1319-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1319-129">RELATED LINKS</span></span>

[<span data-ttu-id="b1319-130">새로운 AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="b1319-130">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="b1319-131">제거-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="b1319-131">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
