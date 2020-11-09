---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307658"
---
# <span data-ttu-id="a58f1-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a58f1-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="a58f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a58f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a58f1-103">기존 게이트웨이의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="a58f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a58f1-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a58f1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a58f1-105">DESCRIPTION</span></span>
<span data-ttu-id="a58f1-106">**Get-AzApiManagementGatewayKey** cmdlet은 기존 게이트웨이의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="a58f1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a58f1-107">EXAMPLES</span></span>

### <span data-ttu-id="a58f1-108">예제 2: ID로 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="a58f1-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="a58f1-109">이 명령은 "0123456789" 게이트웨이의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="a58f1-110">변수</span><span class="sxs-lookup"><span data-stu-id="a58f1-110">PARAMETERS</span></span>

### <span data-ttu-id="a58f1-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a58f1-111">-Context</span></span>
<span data-ttu-id="a58f1-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a58f1-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a58f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58f1-114">-DefaultProfile</span></span>
<span data-ttu-id="a58f1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a58f1-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a58f1-116">-GatewayId</span></span>
<span data-ttu-id="a58f1-117">게이트웨이 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-117">Gateway identifier.</span></span>
<span data-ttu-id="a58f1-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58f1-119">CommonParameters</span></span>
<span data-ttu-id="a58f1-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58f1-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a58f1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58f1-122">입력</span><span class="sxs-lookup"><span data-stu-id="a58f1-122">INPUTS</span></span>

### <span data-ttu-id="a58f1-123">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a58f1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a58f1-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a58f1-124">System.String</span></span>

## <span data-ttu-id="a58f1-125">출력</span><span class="sxs-lookup"><span data-stu-id="a58f1-125">OUTPUTS</span></span>

### <span data-ttu-id="a58f1-126">ApiManagement. ServiceManagement. \ PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a58f1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="a58f1-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a58f1-127">NOTES</span></span>

## <span data-ttu-id="a58f1-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a58f1-128">RELATED LINKS</span></span>
