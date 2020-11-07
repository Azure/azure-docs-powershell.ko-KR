---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702779"
---
# <span data-ttu-id="85e04-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="85e04-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="85e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85e04-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85e04-103">구문과</span><span class="sxs-lookup"><span data-stu-id="85e04-103">SYNTAX</span></span>

### <span data-ttu-id="85e04-104">모든 속성 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="85e04-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85e04-105">Get by 속성 ID</span><span class="sxs-lookup"><span data-stu-id="85e04-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85e04-106">이름을 포함 하는 속성 찾기</span><span class="sxs-lookup"><span data-stu-id="85e04-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85e04-107">태그별 속성 찾기</span><span class="sxs-lookup"><span data-stu-id="85e04-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85e04-108">설명은</span><span class="sxs-lookup"><span data-stu-id="85e04-108">DESCRIPTION</span></span>

## <span data-ttu-id="85e04-109">예제의</span><span class="sxs-lookup"><span data-stu-id="85e04-109">EXAMPLES</span></span>

### <span data-ttu-id="85e04-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="85e04-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="85e04-111">변수</span><span class="sxs-lookup"><span data-stu-id="85e04-111">PARAMETERS</span></span>

### <span data-ttu-id="85e04-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="85e04-112">-Context</span></span>
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

### <span data-ttu-id="85e04-113">-이름</span><span class="sxs-lookup"><span data-stu-id="85e04-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e04-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="85e04-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e04-115">태그</span><span class="sxs-lookup"><span data-stu-id="85e04-115">-Tag</span></span>
<span data-ttu-id="85e04-116">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="85e04-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85e04-117">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="85e04-117">For example:</span></span>

<span data-ttu-id="85e04-118">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="85e04-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e04-119">-DefaultProfile</span></span>
<span data-ttu-id="85e04-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85e04-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85e04-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e04-121">CommonParameters</span></span>
<span data-ttu-id="85e04-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e04-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e04-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e04-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e04-124">입력</span><span class="sxs-lookup"><span data-stu-id="85e04-124">INPUTS</span></span>

## <span data-ttu-id="85e04-125">출력</span><span class="sxs-lookup"><span data-stu-id="85e04-125">OUTPUTS</span></span>

### <span data-ttu-id="85e04-126">System.webserver. t e ServiceManagement의 경우 ' 1 [ApiManagement]. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="85e04-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="85e04-127">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="85e04-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="85e04-128">상속자</span><span class="sxs-lookup"><span data-stu-id="85e04-128">NOTES</span></span>

## <span data-ttu-id="85e04-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85e04-129">RELATED LINKS</span></span>

