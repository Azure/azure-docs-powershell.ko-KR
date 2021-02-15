---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182364"
---
# <span data-ttu-id="47817-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="47817-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="47817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47817-102">SYNOPSIS</span></span>
<span data-ttu-id="47817-103">Git 분기의 변경 내용을 구성 데이터베이스에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="47817-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="47817-104">구문</span><span class="sxs-lookup"><span data-stu-id="47817-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47817-105">설명</span><span class="sxs-lookup"><span data-stu-id="47817-105">DESCRIPTION</span></span>
<span data-ttu-id="47817-106">**Publish-AzApiManagementTenantGitConfiguration** cmdlet은 Git 분기의 변경 내용을 구성 데이터베이스에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="47817-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="47817-107">또는 게시하지 않고 Git 분기에서 변경 내용의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47817-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="47817-108">예제</span><span class="sxs-lookup"><span data-stu-id="47817-108">EXAMPLES</span></span>

### <span data-ttu-id="47817-109">예제 1: Git 변경 내용 배포</span><span class="sxs-lookup"><span data-stu-id="47817-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="47817-110">이 명령은 지정된 분기의 변경 내용을 구성 데이터베이스에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="47817-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="47817-111">예제 2: Git 변경 내용 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="47817-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="47817-112">이 명령은 구성 데이터베이스에 대해 Git 분기의 변경 내용의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="47817-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="47817-113">변경 내용을 게시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47817-113">It does not publish changes.</span></span>

## <span data-ttu-id="47817-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47817-114">PARAMETERS</span></span>

### <span data-ttu-id="47817-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="47817-115">-Branch</span></span>
<span data-ttu-id="47817-116">이 cmdlet이 구성 데이터베이스에 구성을 배포하는 Git 분기의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47817-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="47817-117">-Context</span><span class="sxs-lookup"><span data-stu-id="47817-117">-Context</span></span>
<span data-ttu-id="47817-118">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="47817-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="47817-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47817-119">-DefaultProfile</span></span>
<span data-ttu-id="47817-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47817-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47817-121">-Force</span><span class="sxs-lookup"><span data-stu-id="47817-121">-Force</span></span>
<span data-ttu-id="47817-122">이 cmdlet이 이 업데이트에서 삭제된 제품에 대한 구독을 삭제하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="47817-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="47817-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47817-123">-PassThru</span></span>
<span data-ttu-id="47817-124">이 cmdlet이 **PsApiManagementOperationResult 개체를 반환하는지 나타냅니다.**</span><span class="sxs-lookup"><span data-stu-id="47817-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="47817-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="47817-125">-ValidateOnly</span></span>
<span data-ttu-id="47817-126">이 cmdlet이 지정된 Git 분기의 변경 내용의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="47817-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="47817-127">구성 데이터베이스에 게시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47817-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="47817-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47817-128">-Confirm</span></span>
<span data-ttu-id="47817-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47817-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47817-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47817-130">-WhatIf</span></span>
<span data-ttu-id="47817-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="47817-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47817-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47817-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47817-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47817-133">CommonParameters</span></span>
<span data-ttu-id="47817-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47817-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47817-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47817-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47817-136">입력</span><span class="sxs-lookup"><span data-stu-id="47817-136">INPUTS</span></span>

### <span data-ttu-id="47817-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47817-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47817-138">System.String</span><span class="sxs-lookup"><span data-stu-id="47817-138">System.String</span></span>

### <span data-ttu-id="47817-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47817-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47817-140">출력</span><span class="sxs-lookup"><span data-stu-id="47817-140">OUTPUTS</span></span>

### <span data-ttu-id="47817-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="47817-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="47817-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47817-142">NOTES</span></span>

## <span data-ttu-id="47817-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47817-143">RELATED LINKS</span></span>

[<span data-ttu-id="47817-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="47817-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


