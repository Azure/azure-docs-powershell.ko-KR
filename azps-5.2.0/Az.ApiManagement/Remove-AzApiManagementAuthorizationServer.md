---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330170"
---
# <span data-ttu-id="47561-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47561-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="47561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47561-102">SYNOPSIS</span></span>
<span data-ttu-id="47561-103">권한 부여 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="47561-103">Removes an authorization server.</span></span>

## <span data-ttu-id="47561-104">구문</span><span class="sxs-lookup"><span data-stu-id="47561-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47561-105">설명</span><span class="sxs-lookup"><span data-stu-id="47561-105">DESCRIPTION</span></span>
<span data-ttu-id="47561-106">**Remove-AzApiManagementAuthorizationServer** cmdlet은 Azure API Management 권한 부여 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="47561-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="47561-107">예제</span><span class="sxs-lookup"><span data-stu-id="47561-107">EXAMPLES</span></span>

### <span data-ttu-id="47561-108">예제 1: 권한 부여 서버 제거</span><span class="sxs-lookup"><span data-stu-id="47561-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="47561-109">이 명령은 지정된 API Management 권한 부여 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="47561-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="47561-110">Force 매개 *변수가* 지정되어 있기 때문에 확인이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47561-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="47561-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47561-111">PARAMETERS</span></span>

### <span data-ttu-id="47561-112">-Context</span><span class="sxs-lookup"><span data-stu-id="47561-112">-Context</span></span>
<span data-ttu-id="47561-113">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="47561-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="47561-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47561-114">-DefaultProfile</span></span>
<span data-ttu-id="47561-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47561-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47561-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47561-116">-PassThru</span></span>
<span data-ttu-id="47561-117">passthru</span><span class="sxs-lookup"><span data-stu-id="47561-117">passthru</span></span>

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

### <span data-ttu-id="47561-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="47561-118">-ServerId</span></span>
<span data-ttu-id="47561-119">제거할 권한 부여 서버의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47561-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="47561-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47561-120">-Confirm</span></span>
<span data-ttu-id="47561-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47561-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47561-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47561-122">-WhatIf</span></span>
<span data-ttu-id="47561-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="47561-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47561-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47561-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47561-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47561-125">CommonParameters</span></span>
<span data-ttu-id="47561-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47561-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47561-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47561-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47561-128">입력</span><span class="sxs-lookup"><span data-stu-id="47561-128">INPUTS</span></span>

### <span data-ttu-id="47561-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47561-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47561-130">System.String</span><span class="sxs-lookup"><span data-stu-id="47561-130">System.String</span></span>

### <span data-ttu-id="47561-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47561-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47561-132">출력</span><span class="sxs-lookup"><span data-stu-id="47561-132">OUTPUTS</span></span>

### <span data-ttu-id="47561-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47561-133">System.Boolean</span></span>

## <span data-ttu-id="47561-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47561-134">NOTES</span></span>

## <span data-ttu-id="47561-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47561-135">RELATED LINKS</span></span>

[<span data-ttu-id="47561-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47561-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="47561-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47561-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="47561-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="47561-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


