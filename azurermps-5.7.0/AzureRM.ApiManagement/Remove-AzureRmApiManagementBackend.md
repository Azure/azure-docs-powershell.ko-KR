---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530584"
---
# <span data-ttu-id="b6115-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b6115-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="b6115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6115-102">SYNOPSIS</span></span>
<span data-ttu-id="b6115-103">백 엔드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6115-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6115-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6115-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6115-105">DESCRIPTION</span></span>
<span data-ttu-id="b6115-106">Api Management에서 식별자로 지정 된 백 엔드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="b6115-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b6115-107">EXAMPLES</span></span>

### <span data-ttu-id="b6115-108">예제 1: 백엔드 123 제거</span><span class="sxs-lookup"><span data-stu-id="b6115-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="b6115-109">변수</span><span class="sxs-lookup"><span data-stu-id="b6115-109">PARAMETERS</span></span>

### <span data-ttu-id="b6115-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="b6115-110">-BackendId</span></span>
<span data-ttu-id="b6115-111">기존 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-111">Identifier of existing backend.</span></span>
<span data-ttu-id="b6115-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-112">This parameter is required.</span></span>

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

### <span data-ttu-id="b6115-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b6115-113">-Context</span></span>
<span data-ttu-id="b6115-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b6115-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-115">This parameter is required.</span></span>

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

### <span data-ttu-id="b6115-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6115-116">-DefaultProfile</span></span>
<span data-ttu-id="b6115-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b6115-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6115-118">-PassThru</span></span>
<span data-ttu-id="b6115-119">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b6115-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-120">This parameter is optional.</span></span>
<span data-ttu-id="b6115-121">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-121">Default value is false.</span></span>

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

### <span data-ttu-id="b6115-122">-확인</span><span class="sxs-lookup"><span data-stu-id="b6115-122">-Confirm</span></span>
<span data-ttu-id="b6115-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6115-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6115-124">-WhatIf</span></span>
<span data-ttu-id="b6115-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6115-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6115-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6115-127">CommonParameters</span></span>
<span data-ttu-id="b6115-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6115-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6115-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6115-130">입력</span><span class="sxs-lookup"><span data-stu-id="b6115-130">INPUTS</span></span>

### <span data-ttu-id="b6115-131">않아야</span><span class="sxs-lookup"><span data-stu-id="b6115-131">None</span></span>
<span data-ttu-id="b6115-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6115-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6115-133">출력</span><span class="sxs-lookup"><span data-stu-id="b6115-133">OUTPUTS</span></span>

### <span data-ttu-id="b6115-134">부울</span><span class="sxs-lookup"><span data-stu-id="b6115-134">bool</span></span>

## <span data-ttu-id="b6115-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b6115-135">NOTES</span></span>

## <span data-ttu-id="b6115-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6115-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6115-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b6115-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="b6115-138">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b6115-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b6115-139">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b6115-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="b6115-140">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b6115-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="b6115-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b6115-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
