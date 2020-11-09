---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308645"
---
# <span data-ttu-id="14579-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="14579-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="14579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14579-102">SYNOPSIS</span></span>
<span data-ttu-id="14579-103">백 엔드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14579-103">Removes a Backend.</span></span>

## <span data-ttu-id="14579-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14579-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14579-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14579-105">DESCRIPTION</span></span>
<span data-ttu-id="14579-106">Api Management에서 식별자로 지정 된 백 엔드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="14579-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="14579-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14579-107">EXAMPLES</span></span>

### <span data-ttu-id="14579-108">예제 1: 백엔드 123 제거</span><span class="sxs-lookup"><span data-stu-id="14579-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="14579-109">변수</span><span class="sxs-lookup"><span data-stu-id="14579-109">PARAMETERS</span></span>

### <span data-ttu-id="14579-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="14579-110">-BackendId</span></span>
<span data-ttu-id="14579-111">기존 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="14579-111">Identifier of existing backend.</span></span>
<span data-ttu-id="14579-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="14579-112">This parameter is required.</span></span>

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

### <span data-ttu-id="14579-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="14579-113">-Context</span></span>
<span data-ttu-id="14579-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="14579-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="14579-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="14579-115">This parameter is required.</span></span>

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

### <span data-ttu-id="14579-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14579-116">-DefaultProfile</span></span>
<span data-ttu-id="14579-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14579-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14579-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14579-118">-PassThru</span></span>
<span data-ttu-id="14579-119">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="14579-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="14579-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="14579-120">This parameter is optional.</span></span>
<span data-ttu-id="14579-121">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="14579-121">Default value is false.</span></span>

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

### <span data-ttu-id="14579-122">-확인</span><span class="sxs-lookup"><span data-stu-id="14579-122">-Confirm</span></span>
<span data-ttu-id="14579-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14579-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14579-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14579-124">-WhatIf</span></span>
<span data-ttu-id="14579-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14579-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14579-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14579-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14579-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14579-127">CommonParameters</span></span>
<span data-ttu-id="14579-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14579-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14579-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14579-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14579-130">입력</span><span class="sxs-lookup"><span data-stu-id="14579-130">INPUTS</span></span>

### <span data-ttu-id="14579-131">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="14579-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="14579-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14579-132">System.String</span></span>

### <span data-ttu-id="14579-133">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="14579-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14579-134">출력</span><span class="sxs-lookup"><span data-stu-id="14579-134">OUTPUTS</span></span>

### <span data-ttu-id="14579-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="14579-135">System.Boolean</span></span>

## <span data-ttu-id="14579-136">상속자</span><span class="sxs-lookup"><span data-stu-id="14579-136">NOTES</span></span>

## <span data-ttu-id="14579-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14579-137">RELATED LINKS</span></span>

[<span data-ttu-id="14579-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="14579-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="14579-139">새로운 AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="14579-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="14579-140">새로운 AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="14579-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="14579-141">새로운 AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="14579-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="14579-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="14579-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
