---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 22cba1b904032ee654b091d1adae541848fd50c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524740"
---
# <span data-ttu-id="000fd-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="000fd-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="000fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="000fd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="000fd-103">구문과</span><span class="sxs-lookup"><span data-stu-id="000fd-103">SYNTAX</span></span>

### <span data-ttu-id="000fd-104">GetAllProperties (기본값)</span><span class="sxs-lookup"><span data-stu-id="000fd-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="000fd-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="000fd-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="000fd-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="000fd-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="000fd-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="000fd-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="000fd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="000fd-108">DESCRIPTION</span></span>

## <span data-ttu-id="000fd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="000fd-109">EXAMPLES</span></span>

### <span data-ttu-id="000fd-110">예제 1: 이름으로 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="000fd-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="000fd-111">변수</span><span class="sxs-lookup"><span data-stu-id="000fd-111">PARAMETERS</span></span>

### <span data-ttu-id="000fd-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="000fd-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000fd-113">-DefaultProfile</span></span>
<span data-ttu-id="000fd-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="000fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="000fd-115">-이름</span><span class="sxs-lookup"><span data-stu-id="000fd-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000fd-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="000fd-116">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000fd-117">태그</span><span class="sxs-lookup"><span data-stu-id="000fd-117">-Tag</span></span>
<span data-ttu-id="000fd-118">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="000fd-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="000fd-119">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="000fd-119">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000fd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000fd-120">CommonParameters</span></span>
<span data-ttu-id="000fd-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="000fd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000fd-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="000fd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000fd-123">입력</span><span class="sxs-lookup"><span data-stu-id="000fd-123">INPUTS</span></span>

### <span data-ttu-id="000fd-124">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="000fd-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="000fd-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="000fd-125">System.String</span></span>

## <span data-ttu-id="000fd-126">출력</span><span class="sxs-lookup"><span data-stu-id="000fd-126">OUTPUTS</span></span>

### <span data-ttu-id="000fd-127">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="000fd-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="000fd-128">상속자</span><span class="sxs-lookup"><span data-stu-id="000fd-128">NOTES</span></span>

## <span data-ttu-id="000fd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="000fd-129">RELATED LINKS</span></span>
