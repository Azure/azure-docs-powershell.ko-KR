---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: d8c47cb6aaf1f135cd08110f4ab1d616cb105f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525392"
---
# <span data-ttu-id="b6110-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6110-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="b6110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6110-102">SYNOPSIS</span></span>
<span data-ttu-id="b6110-103">API Management 속성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6110-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6110-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6110-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6110-105">DESCRIPTION</span></span>
<span data-ttu-id="b6110-106">**AzureRmApiManagementProperty** Cmdlet은 Azure API Management **속성** 을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="b6110-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b6110-107">EXAMPLES</span></span>

### <span data-ttu-id="b6110-108">예제 1: 속성 제거</span><span class="sxs-lookup"><span data-stu-id="b6110-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="b6110-109">이 명령은 ID Property11 인 속성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="b6110-110">변수</span><span class="sxs-lookup"><span data-stu-id="b6110-110">PARAMETERS</span></span>

### <span data-ttu-id="b6110-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b6110-111">-Context</span></span>
<span data-ttu-id="b6110-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b6110-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6110-113">-DefaultProfile</span></span>
<span data-ttu-id="b6110-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b6110-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6110-115">-PassThru</span></span>
<span data-ttu-id="b6110-116">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6110-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="b6110-117">-PropertyId</span></span>
<span data-ttu-id="b6110-118">이 cmdlet이 제거 하는 속성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-118">Specifies an ID of the property that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6110-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b6110-119">-Confirm</span></span>
<span data-ttu-id="b6110-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6110-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6110-121">-WhatIf</span></span>
<span data-ttu-id="b6110-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6110-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6110-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6110-124">CommonParameters</span></span>
<span data-ttu-id="b6110-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6110-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6110-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6110-127">입력</span><span class="sxs-lookup"><span data-stu-id="b6110-127">INPUTS</span></span>

### <span data-ttu-id="b6110-128">않아야</span><span class="sxs-lookup"><span data-stu-id="b6110-128">None</span></span>
<span data-ttu-id="b6110-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6110-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6110-130">출력</span><span class="sxs-lookup"><span data-stu-id="b6110-130">OUTPUTS</span></span>

### <span data-ttu-id="b6110-131">부울</span><span class="sxs-lookup"><span data-stu-id="b6110-131">bool</span></span>

## <span data-ttu-id="b6110-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b6110-132">NOTES</span></span>

## <span data-ttu-id="b6110-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6110-133">RELATED LINKS</span></span>

[<span data-ttu-id="b6110-134">새로운 AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6110-134">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="b6110-135">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6110-135">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


