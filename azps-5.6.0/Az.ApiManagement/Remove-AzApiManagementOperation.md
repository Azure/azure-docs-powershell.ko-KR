---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 0db56d65893c9c003261c2004435c5d231c014f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990593"
---
# <span data-ttu-id="212c9-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="212c9-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="212c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="212c9-102">SYNOPSIS</span></span>
<span data-ttu-id="212c9-103">기존 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-103">Removes an existing operation.</span></span>

## <span data-ttu-id="212c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="212c9-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="212c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="212c9-105">DESCRIPTION</span></span>
<span data-ttu-id="212c9-106">**Remove-AzApiManagementOperation** cmdlet은 기존 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="212c9-107">예제</span><span class="sxs-lookup"><span data-stu-id="212c9-107">EXAMPLES</span></span>

### <span data-ttu-id="212c9-108">예제 1: 기존 API 작업 제거</span><span class="sxs-lookup"><span data-stu-id="212c9-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="212c9-109">이 명령은 기존 API 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="212c9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="212c9-110">PARAMETERS</span></span>

### <span data-ttu-id="212c9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="212c9-111">-ApiId</span></span>
<span data-ttu-id="212c9-112">API의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="212c9-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="212c9-113">-ApiRevision</span></span>
<span data-ttu-id="212c9-114">API 개정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-114">Identifier of API Revision.</span></span> <span data-ttu-id="212c9-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-115">This parameter is optional.</span></span> <span data-ttu-id="212c9-116">지정하지 않으면 현재 활성 API 개정에서 작업이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="212c9-117">-Context</span><span class="sxs-lookup"><span data-stu-id="212c9-117">-Context</span></span>
<span data-ttu-id="212c9-118">**PsApiManagementContext의 인스턴스를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="212c9-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="212c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212c9-119">-DefaultProfile</span></span>
<span data-ttu-id="212c9-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="212c9-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="212c9-121">-OperationId</span></span>
<span data-ttu-id="212c9-122">API 작업의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="212c9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="212c9-123">-PassThru</span></span>
<span data-ttu-id="212c9-124">이 cmdlet은 성공하는 경우 $True 값을 반환하거나, 그렇지 않은 경우 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="212c9-125">-확인</span><span class="sxs-lookup"><span data-stu-id="212c9-125">-Confirm</span></span>
<span data-ttu-id="212c9-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="212c9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212c9-127">-WhatIf</span></span>
<span data-ttu-id="212c9-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212c9-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="212c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212c9-130">CommonParameters</span></span>
<span data-ttu-id="212c9-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="212c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212c9-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="212c9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212c9-133">입력</span><span class="sxs-lookup"><span data-stu-id="212c9-133">INPUTS</span></span>

### <span data-ttu-id="212c9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="212c9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="212c9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="212c9-135">System.String</span></span>

### <span data-ttu-id="212c9-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="212c9-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="212c9-137">출력</span><span class="sxs-lookup"><span data-stu-id="212c9-137">OUTPUTS</span></span>

### <span data-ttu-id="212c9-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="212c9-138">System.Boolean</span></span>

## <span data-ttu-id="212c9-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="212c9-139">NOTES</span></span>

## <span data-ttu-id="212c9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="212c9-140">RELATED LINKS</span></span>

[<span data-ttu-id="212c9-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="212c9-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="212c9-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="212c9-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="212c9-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="212c9-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


