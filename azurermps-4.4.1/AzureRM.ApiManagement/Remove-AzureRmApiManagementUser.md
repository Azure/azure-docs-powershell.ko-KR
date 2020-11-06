---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525748"
---
# <span data-ttu-id="68cd0-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="68cd0-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="68cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="68cd0-103">기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68cd0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68cd0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68cd0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="68cd0-106">**제거-AzureRmApiManagementUser** cmdlet은 기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="68cd0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="68cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="68cd0-108">예제 1: 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="68cd0-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="68cd0-109">이 명령은 기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="68cd0-110">변수</span><span class="sxs-lookup"><span data-stu-id="68cd0-110">PARAMETERS</span></span>

### <span data-ttu-id="68cd0-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="68cd0-111">-Context</span></span>
<span data-ttu-id="68cd0-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="68cd0-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="68cd0-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="68cd0-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="68cd0-115">제품에 대 한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="68cd0-116">이 매개 변수를 지정 하지 않고 구독이 있으면이 cmdlet은 예외를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="68cd0-117">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-117">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68cd0-118">-PassThru</span></span>
<span data-ttu-id="68cd0-119">이 cmdlet이 $Ture 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd0-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="68cd0-120">-UserId</span></span>
<span data-ttu-id="68cd0-121">제거할 사용자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="68cd0-122">-확인</span><span class="sxs-lookup"><span data-stu-id="68cd0-122">-Confirm</span></span>
<span data-ttu-id="68cd0-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cd0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68cd0-124">-WhatIf</span></span>
<span data-ttu-id="68cd0-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68cd0-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cd0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cd0-127">-DefaultProfile</span></span>
<span data-ttu-id="68cd0-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68cd0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cd0-129">CommonParameters</span></span>
<span data-ttu-id="68cd0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cd0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cd0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68cd0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cd0-132">입력</span><span class="sxs-lookup"><span data-stu-id="68cd0-132">INPUTS</span></span>

## <span data-ttu-id="68cd0-133">출력</span><span class="sxs-lookup"><span data-stu-id="68cd0-133">OUTPUTS</span></span>

### <span data-ttu-id="68cd0-134">나타내는</span><span class="sxs-lookup"><span data-stu-id="68cd0-134">Boolean</span></span>

## <span data-ttu-id="68cd0-135">상속자</span><span class="sxs-lookup"><span data-stu-id="68cd0-135">NOTES</span></span>

## <span data-ttu-id="68cd0-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68cd0-136">RELATED LINKS</span></span>

[<span data-ttu-id="68cd0-137">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="68cd0-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="68cd0-138">새로운 AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="68cd0-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="68cd0-139">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="68cd0-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


