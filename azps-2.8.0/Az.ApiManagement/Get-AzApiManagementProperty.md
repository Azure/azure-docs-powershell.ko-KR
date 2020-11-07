---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: 2c8fc24d252fce12e7adf9ee824db0e1b2c8b206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698098"
---
# <span data-ttu-id="5a821-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="5a821-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="5a821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a821-102">SYNOPSIS</span></span>
<span data-ttu-id="5a821-103">목록 또는 특정 속성 (명명 된 값)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a821-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="5a821-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a821-104">SYNTAX</span></span>

### <span data-ttu-id="5a821-105">GetAllProperties (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a821-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a821-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="5a821-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a821-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="5a821-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a821-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="5a821-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a821-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5a821-109">DESCRIPTION</span></span>
<span data-ttu-id="5a821-110">**Get-AzApiManagementProperty** cmdlet은 목록 또는 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a821-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="5a821-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5a821-111">EXAMPLES</span></span>

### <span data-ttu-id="5a821-112">예제 1: 이름으로 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="5a821-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="5a821-113">변수</span><span class="sxs-lookup"><span data-stu-id="5a821-113">PARAMETERS</span></span>

### <span data-ttu-id="5a821-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5a821-114">-Context</span></span>
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

### <span data-ttu-id="5a821-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a821-115">-DefaultProfile</span></span>
<span data-ttu-id="5a821-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a821-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a821-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5a821-117">-Name</span></span>
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

### <span data-ttu-id="5a821-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="5a821-118">-PropertyId</span></span>
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

### <span data-ttu-id="5a821-119">태그</span><span class="sxs-lookup"><span data-stu-id="5a821-119">-Tag</span></span>
<span data-ttu-id="5a821-120">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5a821-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5a821-121">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5a821-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5a821-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a821-122">CommonParameters</span></span>
<span data-ttu-id="5a821-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a821-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a821-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5a821-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a821-125">입력</span><span class="sxs-lookup"><span data-stu-id="5a821-125">INPUTS</span></span>

### <span data-ttu-id="5a821-126">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5a821-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a821-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a821-127">System.String</span></span>

## <span data-ttu-id="5a821-128">출력</span><span class="sxs-lookup"><span data-stu-id="5a821-128">OUTPUTS</span></span>

### <span data-ttu-id="5a821-129">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="5a821-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="5a821-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5a821-130">NOTES</span></span>

## <span data-ttu-id="5a821-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a821-131">RELATED LINKS</span></span>
