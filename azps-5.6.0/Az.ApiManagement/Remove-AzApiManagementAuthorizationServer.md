---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 8cbb9afc37242330bc76b7413033dc41cbd61cd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973003"
---
# <span data-ttu-id="df7b1-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df7b1-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="df7b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="df7b1-103">권한 부여 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-103">Removes an authorization server.</span></span>

## <span data-ttu-id="df7b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="df7b1-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df7b1-105">설명</span><span class="sxs-lookup"><span data-stu-id="df7b1-105">DESCRIPTION</span></span>
<span data-ttu-id="df7b1-106">**Remove-AzApiManagementAuthorizationServer** cmdlet은 Azure API Management 권한 부여 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="df7b1-107">예제</span><span class="sxs-lookup"><span data-stu-id="df7b1-107">EXAMPLES</span></span>

### <span data-ttu-id="df7b1-108">예제 1: 권한 부여 서버 제거</span><span class="sxs-lookup"><span data-stu-id="df7b1-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="df7b1-109">이 명령은 지정된 API Management 권한 부여 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="df7b1-110">Force *매개* 변수가 지정되어 있기 때문에 확인이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="df7b1-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="df7b1-111">PARAMETERS</span></span>

### <span data-ttu-id="df7b1-112">-Context</span><span class="sxs-lookup"><span data-stu-id="df7b1-112">-Context</span></span>
<span data-ttu-id="df7b1-113">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="df7b1-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="df7b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7b1-114">-DefaultProfile</span></span>
<span data-ttu-id="df7b1-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df7b1-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df7b1-116">-PassThru</span></span>
<span data-ttu-id="df7b1-117">passthru</span><span class="sxs-lookup"><span data-stu-id="df7b1-117">passthru</span></span>

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

### <span data-ttu-id="df7b1-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="df7b1-118">-ServerId</span></span>
<span data-ttu-id="df7b1-119">제거할 권한 부여 서버의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="df7b1-120">-확인</span><span class="sxs-lookup"><span data-stu-id="df7b1-120">-Confirm</span></span>
<span data-ttu-id="df7b1-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7b1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7b1-122">-WhatIf</span></span>
<span data-ttu-id="df7b1-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7b1-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7b1-125">CommonParameters</span></span>
<span data-ttu-id="df7b1-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df7b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7b1-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df7b1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7b1-128">입력</span><span class="sxs-lookup"><span data-stu-id="df7b1-128">INPUTS</span></span>

### <span data-ttu-id="df7b1-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="df7b1-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="df7b1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="df7b1-130">System.String</span></span>

### <span data-ttu-id="df7b1-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df7b1-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df7b1-132">출력</span><span class="sxs-lookup"><span data-stu-id="df7b1-132">OUTPUTS</span></span>

### <span data-ttu-id="df7b1-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df7b1-133">System.Boolean</span></span>

## <span data-ttu-id="df7b1-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df7b1-134">NOTES</span></span>

## <span data-ttu-id="df7b1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df7b1-135">RELATED LINKS</span></span>

[<span data-ttu-id="df7b1-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df7b1-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="df7b1-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df7b1-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="df7b1-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="df7b1-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


