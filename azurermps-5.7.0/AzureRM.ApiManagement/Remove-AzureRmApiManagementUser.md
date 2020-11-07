---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 5d657610ddce1c0397a5f9e8c11b832b3fcd472b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711842"
---
# <span data-ttu-id="36df8-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="36df8-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="36df8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36df8-102">SYNOPSIS</span></span>
<span data-ttu-id="36df8-103">기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36df8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36df8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36df8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="36df8-105">DESCRIPTION</span></span>
<span data-ttu-id="36df8-106">**제거-AzureRmApiManagementUser** cmdlet은 기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="36df8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="36df8-107">EXAMPLES</span></span>

### <span data-ttu-id="36df8-108">예제 1: 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="36df8-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="36df8-109">이 명령은 기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="36df8-110">변수</span><span class="sxs-lookup"><span data-stu-id="36df8-110">PARAMETERS</span></span>

### <span data-ttu-id="36df8-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="36df8-111">-Context</span></span>
<span data-ttu-id="36df8-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="36df8-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-113">This parameter is required.</span></span>

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

### <span data-ttu-id="36df8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36df8-114">-DefaultProfile</span></span>
<span data-ttu-id="36df8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="36df8-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="36df8-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="36df8-117">제품에 대 한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="36df8-118">이 매개 변수를 지정 하지 않고 구독이 있으면이 cmdlet은 예외를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="36df8-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="36df8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36df8-120">-PassThru</span></span>
<span data-ttu-id="36df8-121">이 cmdlet이 $Ture 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="36df8-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="36df8-122">-UserId</span></span>
<span data-ttu-id="36df8-123">제거할 사용자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="36df8-124">-확인</span><span class="sxs-lookup"><span data-stu-id="36df8-124">-Confirm</span></span>
<span data-ttu-id="36df8-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36df8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36df8-126">-WhatIf</span></span>
<span data-ttu-id="36df8-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36df8-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36df8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36df8-129">CommonParameters</span></span>
<span data-ttu-id="36df8-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36df8-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36df8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36df8-132">입력</span><span class="sxs-lookup"><span data-stu-id="36df8-132">INPUTS</span></span>

### <span data-ttu-id="36df8-133">않아야</span><span class="sxs-lookup"><span data-stu-id="36df8-133">None</span></span>
<span data-ttu-id="36df8-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36df8-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36df8-135">출력</span><span class="sxs-lookup"><span data-stu-id="36df8-135">OUTPUTS</span></span>

### <span data-ttu-id="36df8-136">나타내는</span><span class="sxs-lookup"><span data-stu-id="36df8-136">Boolean</span></span>

## <span data-ttu-id="36df8-137">상속자</span><span class="sxs-lookup"><span data-stu-id="36df8-137">NOTES</span></span>

## <span data-ttu-id="36df8-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36df8-138">RELATED LINKS</span></span>

[<span data-ttu-id="36df8-139">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="36df8-139">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="36df8-140">새로운 AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="36df8-140">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="36df8-141">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="36df8-141">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


