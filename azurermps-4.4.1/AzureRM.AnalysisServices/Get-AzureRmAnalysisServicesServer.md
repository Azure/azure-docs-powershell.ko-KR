---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f80f3eead528c7731007bcd6611f5d6fecbb55e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527752"
---
# <span data-ttu-id="5ed52-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5ed52-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="5ed52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ed52-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed52-103">Analysis Services 서버에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ed52-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ed52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ed52-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ed52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ed52-105">DESCRIPTION</span></span>
<span data-ttu-id="5ed52-106">Get-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ed52-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="5ed52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5ed52-107">EXAMPLES</span></span>

### <span data-ttu-id="5ed52-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ed52-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="5ed52-109">이 명령은 ResourceGroup03 이라는 리소스 그룹의 모든 Azure Analysis Services 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ed52-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="5ed52-110">예제 2: 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="5ed52-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="5ed52-111">이 명령은 ResourceGroup03 이라는 리소스 그룹에서 testserver 라는 Azure Analysis Services 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ed52-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="5ed52-112">변수</span><span class="sxs-lookup"><span data-stu-id="5ed52-112">PARAMETERS</span></span>

### <span data-ttu-id="5ed52-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5ed52-113">-Name</span></span>
<span data-ttu-id="5ed52-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ed52-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="5ed52-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed52-115">-ResourceGroupName</span></span>
<span data-ttu-id="5ed52-116">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5ed52-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed52-117">-DefaultProfile</span></span>
<span data-ttu-id="5ed52-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ed52-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed52-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed52-119">CommonParameters</span></span>
<span data-ttu-id="5ed52-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed52-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed52-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed52-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed52-122">입력</span><span class="sxs-lookup"><span data-stu-id="5ed52-122">INPUTS</span></span>

## <span data-ttu-id="5ed52-123">출력</span><span class="sxs-lookup"><span data-stu-id="5ed52-123">OUTPUTS</span></span>

### <span data-ttu-id="5ed52-124">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="5ed52-124">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="5ed52-125">상속자</span><span class="sxs-lookup"><span data-stu-id="5ed52-125">NOTES</span></span>
<span data-ttu-id="5ed52-126">별칭: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="5ed52-126">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="5ed52-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ed52-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ed52-128">새로운 AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="5ed52-128">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="5ed52-129">제거-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="5ed52-129">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
