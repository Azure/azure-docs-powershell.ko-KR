---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535364"
---
# <span data-ttu-id="237e7-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="237e7-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="237e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="237e7-102">SYNOPSIS</span></span>
<span data-ttu-id="237e7-103">기존 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="237e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="237e7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="237e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="237e7-105">DESCRIPTION</span></span>
<span data-ttu-id="237e7-106">**AzureRmApiManagementOperation** cmdlet에서는 기존 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="237e7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="237e7-107">EXAMPLES</span></span>

### <span data-ttu-id="237e7-108">예제 1: 기존 API 연산 제거</span><span class="sxs-lookup"><span data-stu-id="237e7-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="237e7-109">이 명령은 기존 API 연산을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="237e7-110">변수</span><span class="sxs-lookup"><span data-stu-id="237e7-110">PARAMETERS</span></span>

### <span data-ttu-id="237e7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="237e7-111">-ApiId</span></span>
<span data-ttu-id="237e7-112">API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="237e7-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="237e7-113">-Context</span></span>
<span data-ttu-id="237e7-114">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="237e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237e7-115">-DefaultProfile</span></span>
<span data-ttu-id="237e7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="237e7-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="237e7-117">-OperationId</span></span>
<span data-ttu-id="237e7-118">API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-118">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="237e7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="237e7-119">-PassThru</span></span>
<span data-ttu-id="237e7-120">이 cmdlet이 성공할 경우 $True 값을 반환 하거나, $False 값이 없는 경우, 그렇지 않은 경우이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="237e7-121">-확인</span><span class="sxs-lookup"><span data-stu-id="237e7-121">-Confirm</span></span>
<span data-ttu-id="237e7-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="237e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="237e7-123">-WhatIf</span></span>
<span data-ttu-id="237e7-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="237e7-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="237e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237e7-126">CommonParameters</span></span>
<span data-ttu-id="237e7-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237e7-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="237e7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237e7-129">입력</span><span class="sxs-lookup"><span data-stu-id="237e7-129">INPUTS</span></span>

### <span data-ttu-id="237e7-130">않아야</span><span class="sxs-lookup"><span data-stu-id="237e7-130">None</span></span>
<span data-ttu-id="237e7-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="237e7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="237e7-132">출력</span><span class="sxs-lookup"><span data-stu-id="237e7-132">OUTPUTS</span></span>

### <span data-ttu-id="237e7-133">부울</span><span class="sxs-lookup"><span data-stu-id="237e7-133">bool</span></span>

## <span data-ttu-id="237e7-134">상속자</span><span class="sxs-lookup"><span data-stu-id="237e7-134">NOTES</span></span>

## <span data-ttu-id="237e7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="237e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="237e7-136">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="237e7-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="237e7-137">새로운 AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="237e7-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="237e7-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="237e7-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


