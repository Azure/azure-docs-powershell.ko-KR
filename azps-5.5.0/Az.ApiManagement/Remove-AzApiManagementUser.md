---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178033"
---
# <span data-ttu-id="337e6-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="337e6-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="337e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="337e6-102">SYNOPSIS</span></span>
<span data-ttu-id="337e6-103">기존 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-103">Deletes an existing user.</span></span>

## <span data-ttu-id="337e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="337e6-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="337e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="337e6-105">DESCRIPTION</span></span>
<span data-ttu-id="337e6-106">**Remove-AzApiManagementUser** cmdlet은 기존 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="337e6-107">예제</span><span class="sxs-lookup"><span data-stu-id="337e6-107">EXAMPLES</span></span>

### <span data-ttu-id="337e6-108">예제 1: 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="337e6-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="337e6-109">이 명령은 기존 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="337e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="337e6-110">PARAMETERS</span></span>

### <span data-ttu-id="337e6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="337e6-111">-Context</span></span>
<span data-ttu-id="337e6-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="337e6-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="337e6-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-113">This parameter is required.</span></span>

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

### <span data-ttu-id="337e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337e6-114">-DefaultProfile</span></span>
<span data-ttu-id="337e6-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="337e6-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="337e6-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="337e6-117">제품에 대한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="337e6-118">이 매개 변수가 지정되지 않은 경우 구독이 있는 경우 이 cmdlet은 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="337e6-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="337e6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="337e6-120">-PassThru</span></span>
<span data-ttu-id="337e6-121">이 cmdlet이 성공하는 경우 $Ture 값 또는 $False 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="337e6-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="337e6-122">-UserId</span></span>
<span data-ttu-id="337e6-123">제거할 사용자의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="337e6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="337e6-124">-Confirm</span></span>
<span data-ttu-id="337e6-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="337e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="337e6-126">-WhatIf</span></span>
<span data-ttu-id="337e6-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="337e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="337e6-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="337e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337e6-129">CommonParameters</span></span>
<span data-ttu-id="337e6-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="337e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337e6-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="337e6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337e6-132">입력</span><span class="sxs-lookup"><span data-stu-id="337e6-132">INPUTS</span></span>

### <span data-ttu-id="337e6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="337e6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="337e6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="337e6-134">System.String</span></span>

### <span data-ttu-id="337e6-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="337e6-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="337e6-136">출력</span><span class="sxs-lookup"><span data-stu-id="337e6-136">OUTPUTS</span></span>

### <span data-ttu-id="337e6-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="337e6-137">System.Boolean</span></span>

## <span data-ttu-id="337e6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="337e6-138">NOTES</span></span>

## <span data-ttu-id="337e6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="337e6-139">RELATED LINKS</span></span>

[<span data-ttu-id="337e6-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="337e6-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="337e6-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="337e6-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="337e6-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="337e6-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


