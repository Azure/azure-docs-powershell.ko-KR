---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326878"
---
# <span data-ttu-id="80b50-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="80b50-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="80b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80b50-102">SYNOPSIS</span></span>
<span data-ttu-id="80b50-103">Git 분기의 변경 내용을 구성 데이터베이스에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="80b50-104">구문</span><span class="sxs-lookup"><span data-stu-id="80b50-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80b50-105">설명</span><span class="sxs-lookup"><span data-stu-id="80b50-105">DESCRIPTION</span></span>
<span data-ttu-id="80b50-106">**Publish-AzApiManagementTenantGitConfiguration** cmdlet은 Git 분기의 변경 내용을 구성 데이터베이스에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="80b50-107">또는 게시하지 않고 Git 분기에서 변경 내용의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="80b50-108">예제</span><span class="sxs-lookup"><span data-stu-id="80b50-108">EXAMPLES</span></span>

### <span data-ttu-id="80b50-109">예제 1: Git 변경 내용 배포</span><span class="sxs-lookup"><span data-stu-id="80b50-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="80b50-110">이 명령은 지정된 분기의 변경 내용을 구성 데이터베이스에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="80b50-111">예제 2: Git 변경 내용 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="80b50-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="80b50-112">이 명령은 구성 데이터베이스에 대해 Git 분기의 변경 내용의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="80b50-113">변경 내용을 게시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-113">It does not publish changes.</span></span>

## <span data-ttu-id="80b50-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80b50-114">PARAMETERS</span></span>

### <span data-ttu-id="80b50-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="80b50-115">-Branch</span></span>
<span data-ttu-id="80b50-116">이 cmdlet이 구성 데이터베이스에 구성을 배포하는 Git 분기의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="80b50-117">-Context</span><span class="sxs-lookup"><span data-stu-id="80b50-117">-Context</span></span>
<span data-ttu-id="80b50-118">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="80b50-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b50-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b50-119">-DefaultProfile</span></span>
<span data-ttu-id="80b50-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80b50-121">-Force</span><span class="sxs-lookup"><span data-stu-id="80b50-121">-Force</span></span>
<span data-ttu-id="80b50-122">이 cmdlet이 이 업데이트에서 삭제된 제품에 대한 구독을 삭제하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="80b50-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80b50-123">-PassThru</span></span>
<span data-ttu-id="80b50-124">이 cmdlet이 **PsApiManagementOperationResult 개체를 반환하는지 나타냅니다.**</span><span class="sxs-lookup"><span data-stu-id="80b50-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="80b50-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="80b50-125">-ValidateOnly</span></span>
<span data-ttu-id="80b50-126">이 cmdlet이 지정된 Git 분기의 변경 내용의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="80b50-127">구성 데이터베이스에 게시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="80b50-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80b50-128">-Confirm</span></span>
<span data-ttu-id="80b50-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b50-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b50-130">-WhatIf</span></span>
<span data-ttu-id="80b50-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="80b50-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b50-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b50-133">CommonParameters</span></span>
<span data-ttu-id="80b50-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80b50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b50-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80b50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b50-136">입력</span><span class="sxs-lookup"><span data-stu-id="80b50-136">INPUTS</span></span>

### <span data-ttu-id="80b50-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80b50-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80b50-138">System.String</span><span class="sxs-lookup"><span data-stu-id="80b50-138">System.String</span></span>

### <span data-ttu-id="80b50-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80b50-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80b50-140">출력</span><span class="sxs-lookup"><span data-stu-id="80b50-140">OUTPUTS</span></span>

### <span data-ttu-id="80b50-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="80b50-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="80b50-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80b50-142">NOTES</span></span>

## <span data-ttu-id="80b50-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80b50-143">RELATED LINKS</span></span>

[<span data-ttu-id="80b50-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="80b50-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


