---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: 6e5c8dccf2c6694511b21a05590415ab1a6bd126
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689199"
---
# <span data-ttu-id="4bb00-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bb00-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="4bb00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb00-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb00-103">Analysis Services 서버에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bb00-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="4bb00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bb00-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bb00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4bb00-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb00-106">Get-AzAnalysisServicesServer cmdlet은 Analysis Services 서버의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bb00-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="4bb00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4bb00-107">EXAMPLES</span></span>

### <span data-ttu-id="4bb00-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bb00-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="4bb00-109">이 명령은 ResourceGroup03 이라는 리소스 그룹의 모든 Azure Analysis Services 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bb00-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="4bb00-110">예제 2: 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="4bb00-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="4bb00-111">이 명령은 ResourceGroup03 이라는 리소스 그룹에서 testserver 라는 Azure Analysis Services 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bb00-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="4bb00-112">변수</span><span class="sxs-lookup"><span data-stu-id="4bb00-112">PARAMETERS</span></span>

### <span data-ttu-id="4bb00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb00-113">-DefaultProfile</span></span>
<span data-ttu-id="4bb00-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bb00-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4bb00-115">-Name</span></span>
<span data-ttu-id="4bb00-116">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb00-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4bb00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb00-117">-ResourceGroupName</span></span>
<span data-ttu-id="4bb00-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="4bb00-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="4bb00-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb00-119">CommonParameters</span></span>
<span data-ttu-id="4bb00-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb00-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb00-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb00-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb00-122">입력</span><span class="sxs-lookup"><span data-stu-id="4bb00-122">INPUTS</span></span>

### <span data-ttu-id="4bb00-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4bb00-123">System.String</span></span>

## <span data-ttu-id="4bb00-124">출력</span><span class="sxs-lookup"><span data-stu-id="4bb00-124">OUTPUTS</span></span>

### <span data-ttu-id="4bb00-125">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="4bb00-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="4bb00-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4bb00-126">NOTES</span></span>
<span data-ttu-id="4bb00-127">별칭: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="4bb00-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="4bb00-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bb00-128">RELATED LINKS</span></span>

[<span data-ttu-id="4bb00-129">새로운 AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="4bb00-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="4bb00-130">제거-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="4bb00-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
