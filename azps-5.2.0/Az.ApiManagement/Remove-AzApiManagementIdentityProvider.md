---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361369"
---
# <span data-ttu-id="c8237-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c8237-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c8237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8237-102">SYNOPSIS</span></span>
<span data-ttu-id="c8237-103">기존 ID 공급자 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="c8237-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8237-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8237-105">설명</span><span class="sxs-lookup"><span data-stu-id="c8237-105">DESCRIPTION</span></span>
<span data-ttu-id="c8237-106">기존 ID 공급자 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="c8237-107">예제</span><span class="sxs-lookup"><span data-stu-id="c8237-107">EXAMPLES</span></span>

### <span data-ttu-id="c8237-108">예제 1: ApiManagement 서비스에서 Facebook ID 공급자 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="c8237-109">Facebook ID 공급자 구성과 관련된 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="c8237-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8237-110">PARAMETERS</span></span>

### <span data-ttu-id="c8237-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c8237-111">-Context</span></span>
<span data-ttu-id="c8237-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c8237-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c8237-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8237-114">-DefaultProfile</span></span>
<span data-ttu-id="c8237-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8237-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8237-116">-PassThru</span></span>
<span data-ttu-id="c8237-117">작업이 성공하거나 그렇지 않은 경우 이 cmdlet이 $True 값을 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="c8237-118">-Type</span><span class="sxs-lookup"><span data-stu-id="c8237-118">-Type</span></span>
<span data-ttu-id="c8237-119">기존 ID 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="c8237-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8237-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8237-121">-Confirm</span></span>
<span data-ttu-id="c8237-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8237-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8237-123">-WhatIf</span></span>
<span data-ttu-id="c8237-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c8237-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8237-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8237-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8237-126">CommonParameters</span></span>
<span data-ttu-id="c8237-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8237-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8237-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8237-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8237-129">입력</span><span class="sxs-lookup"><span data-stu-id="c8237-129">INPUTS</span></span>

### <span data-ttu-id="c8237-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c8237-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c8237-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="c8237-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="c8237-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8237-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8237-133">출력</span><span class="sxs-lookup"><span data-stu-id="c8237-133">OUTPUTS</span></span>

### <span data-ttu-id="c8237-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8237-134">System.Boolean</span></span>

## <span data-ttu-id="c8237-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8237-135">NOTES</span></span>

## <span data-ttu-id="c8237-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8237-136">RELATED LINKS</span></span>

[<span data-ttu-id="c8237-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c8237-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="c8237-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c8237-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="c8237-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c8237-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

