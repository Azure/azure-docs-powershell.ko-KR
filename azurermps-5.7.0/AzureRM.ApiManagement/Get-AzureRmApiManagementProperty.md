---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529962"
---
# <span data-ttu-id="d8f2a-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d8f2a-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="d8f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f2a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8f2a-103">구문과</span><span class="sxs-lookup"><span data-stu-id="d8f2a-103">SYNTAX</span></span>

### <span data-ttu-id="d8f2a-104">GetAllProperties (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8f2a-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8f2a-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="d8f2a-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f2a-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="d8f2a-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8f2a-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="d8f2a-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8f2a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d8f2a-108">DESCRIPTION</span></span>

## <span data-ttu-id="d8f2a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d8f2a-109">EXAMPLES</span></span>

### <span data-ttu-id="d8f2a-110">예제 1: 이름으로 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8f2a-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="d8f2a-111">변수</span><span class="sxs-lookup"><span data-stu-id="d8f2a-111">PARAMETERS</span></span>

### <span data-ttu-id="d8f2a-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d8f2a-112">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f2a-113">-DefaultProfile</span></span>
<span data-ttu-id="d8f2a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8f2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d8f2a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="d8f2a-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f2a-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="d8f2a-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f2a-117">태그</span><span class="sxs-lookup"><span data-stu-id="d8f2a-117">-Tag</span></span>
<span data-ttu-id="d8f2a-118">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="d8f2a-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d8f2a-119">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="d8f2a-119">For example:</span></span>

<span data-ttu-id="d8f2a-120">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d8f2a-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f2a-121">CommonParameters</span></span>
<span data-ttu-id="d8f2a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8f2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f2a-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f2a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f2a-124">입력</span><span class="sxs-lookup"><span data-stu-id="d8f2a-124">INPUTS</span></span>

### <span data-ttu-id="d8f2a-125">않아야</span><span class="sxs-lookup"><span data-stu-id="d8f2a-125">None</span></span>
<span data-ttu-id="d8f2a-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8f2a-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8f2a-127">출력</span><span class="sxs-lookup"><span data-stu-id="d8f2a-127">OUTPUTS</span></span>

### <span data-ttu-id="d8f2a-128">System.webserver. t e ServiceManagement의 경우 ' 1 [ApiManagement]. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="d8f2a-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="d8f2a-129">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d8f2a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="d8f2a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d8f2a-130">NOTES</span></span>

## <span data-ttu-id="d8f2a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8f2a-131">RELATED LINKS</span></span>

