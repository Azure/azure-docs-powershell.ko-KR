---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 17f7fe4046d5de9dfe288a96a00e8c03486e9c61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959040"
---
# <span data-ttu-id="60c31-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60c31-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="60c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60c31-102">SYNOPSIS</span></span>
<span data-ttu-id="60c31-103">기존 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-103">Deletes an existing user.</span></span>

## <span data-ttu-id="60c31-104">구문</span><span class="sxs-lookup"><span data-stu-id="60c31-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60c31-105">설명</span><span class="sxs-lookup"><span data-stu-id="60c31-105">DESCRIPTION</span></span>
<span data-ttu-id="60c31-106">**Remove-AzApiManagementUser** cmdlet은 기존 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="60c31-107">예제</span><span class="sxs-lookup"><span data-stu-id="60c31-107">EXAMPLES</span></span>

### <span data-ttu-id="60c31-108">예제 1: 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="60c31-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="60c31-109">이 명령은 기존 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="60c31-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="60c31-110">PARAMETERS</span></span>

### <span data-ttu-id="60c31-111">-Context</span><span class="sxs-lookup"><span data-stu-id="60c31-111">-Context</span></span>
<span data-ttu-id="60c31-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="60c31-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="60c31-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-113">This parameter is required.</span></span>

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

### <span data-ttu-id="60c31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c31-114">-DefaultProfile</span></span>
<span data-ttu-id="60c31-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60c31-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="60c31-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="60c31-117">제품에 대한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="60c31-118">이 매개 변수가 지정되지 않은 구독이 있는 경우 이 cmdlet은 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="60c31-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="60c31-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60c31-120">-PassThru</span></span>
<span data-ttu-id="60c31-121">이 cmdlet은 성공하는 경우 $Ture 값을 반환하거나, 그렇지 않은 경우 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="60c31-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="60c31-122">-UserId</span></span>
<span data-ttu-id="60c31-123">제거할 사용자의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="60c31-124">-확인</span><span class="sxs-lookup"><span data-stu-id="60c31-124">-Confirm</span></span>
<span data-ttu-id="60c31-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c31-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c31-126">-WhatIf</span></span>
<span data-ttu-id="60c31-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60c31-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c31-129">CommonParameters</span></span>
<span data-ttu-id="60c31-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60c31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c31-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60c31-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c31-132">입력</span><span class="sxs-lookup"><span data-stu-id="60c31-132">INPUTS</span></span>

### <span data-ttu-id="60c31-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="60c31-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="60c31-134">System.String</span><span class="sxs-lookup"><span data-stu-id="60c31-134">System.String</span></span>

### <span data-ttu-id="60c31-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60c31-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60c31-136">출력</span><span class="sxs-lookup"><span data-stu-id="60c31-136">OUTPUTS</span></span>

### <span data-ttu-id="60c31-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60c31-137">System.Boolean</span></span>

## <span data-ttu-id="60c31-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60c31-138">NOTES</span></span>

## <span data-ttu-id="60c31-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60c31-139">RELATED LINKS</span></span>

[<span data-ttu-id="60c31-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60c31-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="60c31-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60c31-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="60c31-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="60c31-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


