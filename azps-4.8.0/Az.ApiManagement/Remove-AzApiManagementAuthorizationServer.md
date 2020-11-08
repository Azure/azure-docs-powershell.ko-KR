---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056591"
---
# <span data-ttu-id="d6f5d-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d6f5d-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="d6f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f5d-103">권한 부여 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-103">Removes an authorization server.</span></span>

## <span data-ttu-id="d6f5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6f5d-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d6f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f5d-106">**AzApiManagementAuthorizationServer** Cmdlet은 Azure API Management 권한 부여 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="d6f5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d6f5d-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f5d-108">예제 1: 권한 부여 서버 제거</span><span class="sxs-lookup"><span data-stu-id="d6f5d-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="d6f5d-109">이 명령은 지정 된 API 관리 권한 부여 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="d6f5d-110">*Force* 매개 변수는 지정 되어 있으므로 확인이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="d6f5d-111">변수</span><span class="sxs-lookup"><span data-stu-id="d6f5d-111">PARAMETERS</span></span>

### <span data-ttu-id="d6f5d-112">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d6f5d-112">-Context</span></span>
<span data-ttu-id="d6f5d-113">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6f5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f5d-114">-DefaultProfile</span></span>
<span data-ttu-id="d6f5d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6f5d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6f5d-116">-PassThru</span></span>
<span data-ttu-id="d6f5d-117">passthru</span><span class="sxs-lookup"><span data-stu-id="d6f5d-117">passthru</span></span>

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

### <span data-ttu-id="d6f5d-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d6f5d-118">-ServerId</span></span>
<span data-ttu-id="d6f5d-119">제거할 인증 서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="d6f5d-120">-확인</span><span class="sxs-lookup"><span data-stu-id="d6f5d-120">-Confirm</span></span>
<span data-ttu-id="d6f5d-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f5d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f5d-122">-WhatIf</span></span>
<span data-ttu-id="d6f5d-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f5d-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f5d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f5d-125">CommonParameters</span></span>
<span data-ttu-id="d6f5d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f5d-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6f5d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f5d-128">입력</span><span class="sxs-lookup"><span data-stu-id="d6f5d-128">INPUTS</span></span>

### <span data-ttu-id="d6f5d-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6f5d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6f5d-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6f5d-130">System.String</span></span>

### <span data-ttu-id="d6f5d-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6f5d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6f5d-132">출력</span><span class="sxs-lookup"><span data-stu-id="d6f5d-132">OUTPUTS</span></span>

### <span data-ttu-id="d6f5d-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d6f5d-133">System.Boolean</span></span>

## <span data-ttu-id="d6f5d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d6f5d-134">NOTES</span></span>

## <span data-ttu-id="d6f5d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6f5d-135">RELATED LINKS</span></span>

[<span data-ttu-id="d6f5d-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d6f5d-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="d6f5d-137">새로운 AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d6f5d-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="d6f5d-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d6f5d-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


