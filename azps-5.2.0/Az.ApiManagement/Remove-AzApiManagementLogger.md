---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361355"
---
# <span data-ttu-id="d43d4-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d43d4-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="d43d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d43d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d43d4-103">API Management 로거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="d43d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="d43d4-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d43d4-105">설명</span><span class="sxs-lookup"><span data-stu-id="d43d4-105">DESCRIPTION</span></span>
<span data-ttu-id="d43d4-106">**Remove-AzApiManagementLogger** cmdlet은 Azure API Management **로거를 제거합니다.**</span><span class="sxs-lookup"><span data-stu-id="d43d4-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="d43d4-107">예제</span><span class="sxs-lookup"><span data-stu-id="d43d4-107">EXAMPLES</span></span>

### <span data-ttu-id="d43d4-108">예제 1: 로거 제거</span><span class="sxs-lookup"><span data-stu-id="d43d4-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="d43d4-109">이 명령은 ID Logger123이 있는 로거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="d43d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d43d4-110">PARAMETERS</span></span>

### <span data-ttu-id="d43d4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d43d4-111">-Context</span></span>
<span data-ttu-id="d43d4-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="d43d4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d43d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43d4-113">-DefaultProfile</span></span>
<span data-ttu-id="d43d4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d43d4-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d43d4-115">-LoggerId</span></span>
<span data-ttu-id="d43d4-116">제거할 로거의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="d43d4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d43d4-117">-PassThru</span></span>
<span data-ttu-id="d43d4-118">작업이 성공하거나 그렇지 않은 경우 이 cmdlet이 $True 값을 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="d43d4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d43d4-119">-Confirm</span></span>
<span data-ttu-id="d43d4-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d43d4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43d4-121">-WhatIf</span></span>
<span data-ttu-id="d43d4-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d43d4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d43d4-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d43d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43d4-124">CommonParameters</span></span>
<span data-ttu-id="d43d4-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d43d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43d4-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d43d4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43d4-127">입력</span><span class="sxs-lookup"><span data-stu-id="d43d4-127">INPUTS</span></span>

### <span data-ttu-id="d43d4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d43d4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d43d4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d43d4-129">System.String</span></span>

### <span data-ttu-id="d43d4-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d43d4-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d43d4-131">출력</span><span class="sxs-lookup"><span data-stu-id="d43d4-131">OUTPUTS</span></span>

### <span data-ttu-id="d43d4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d43d4-132">System.Boolean</span></span>

## <span data-ttu-id="d43d4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d43d4-133">NOTES</span></span>

## <span data-ttu-id="d43d4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d43d4-134">RELATED LINKS</span></span>

[<span data-ttu-id="d43d4-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d43d4-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="d43d4-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d43d4-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="d43d4-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d43d4-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


