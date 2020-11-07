---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: d9c682f12bd56c2f862396670ce77a8730712279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697964"
---
# <span data-ttu-id="dfcab-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dfcab-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="dfcab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfcab-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcab-103">기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-103">Deletes an existing user.</span></span>

## <span data-ttu-id="dfcab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfcab-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfcab-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcab-106">**제거-AzApiManagementUser** cmdlet은 기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="dfcab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfcab-107">EXAMPLES</span></span>

### <span data-ttu-id="dfcab-108">예제 1: 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="dfcab-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="dfcab-109">이 명령은 기존 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="dfcab-110">변수</span><span class="sxs-lookup"><span data-stu-id="dfcab-110">PARAMETERS</span></span>

### <span data-ttu-id="dfcab-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dfcab-111">-Context</span></span>
<span data-ttu-id="dfcab-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="dfcab-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-113">This parameter is required.</span></span>

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

### <span data-ttu-id="dfcab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcab-114">-DefaultProfile</span></span>
<span data-ttu-id="dfcab-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfcab-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="dfcab-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="dfcab-117">제품에 대 한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="dfcab-118">이 매개 변수를 지정 하지 않고 구독이 있으면이 cmdlet은 예외를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="dfcab-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="dfcab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfcab-120">-PassThru</span></span>
<span data-ttu-id="dfcab-121">이 cmdlet이 $Ture 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="dfcab-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="dfcab-122">-UserId</span></span>
<span data-ttu-id="dfcab-123">제거할 사용자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="dfcab-124">-확인</span><span class="sxs-lookup"><span data-stu-id="dfcab-124">-Confirm</span></span>
<span data-ttu-id="dfcab-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcab-126">-WhatIf</span></span>
<span data-ttu-id="dfcab-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcab-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcab-129">CommonParameters</span></span>
<span data-ttu-id="dfcab-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcab-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfcab-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcab-132">입력</span><span class="sxs-lookup"><span data-stu-id="dfcab-132">INPUTS</span></span>

### <span data-ttu-id="dfcab-133">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dfcab-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dfcab-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfcab-134">System.String</span></span>

### <span data-ttu-id="dfcab-135">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dfcab-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dfcab-136">출력</span><span class="sxs-lookup"><span data-stu-id="dfcab-136">OUTPUTS</span></span>

### <span data-ttu-id="dfcab-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dfcab-137">System.Boolean</span></span>

## <span data-ttu-id="dfcab-138">상속자</span><span class="sxs-lookup"><span data-stu-id="dfcab-138">NOTES</span></span>

## <span data-ttu-id="dfcab-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfcab-139">RELATED LINKS</span></span>

[<span data-ttu-id="dfcab-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dfcab-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="dfcab-141">새로운 AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dfcab-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="dfcab-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dfcab-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


