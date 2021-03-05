---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: eb865535fcb4ee49b834e923fcf3f319ff5de074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965520"
---
# <span data-ttu-id="d0d04-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0d04-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="d0d04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0d04-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d04-103">현재 구성에 대한 커밋을 만들어 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="d0d04-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0d04-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0d04-105">설명</span><span class="sxs-lookup"><span data-stu-id="d0d04-105">DESCRIPTION</span></span>
<span data-ttu-id="d0d04-106">**Save-AzApiManagementTenantGitConfiguration** cmdlet은 리포지토리의 분기에 현재 구성 스냅숏을 포함하는 커밋을 만들어 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="d0d04-107">예제</span><span class="sxs-lookup"><span data-stu-id="d0d04-107">EXAMPLES</span></span>

### <span data-ttu-id="d0d04-108">예제 1: 구성에 변경 내용 저장</span><span class="sxs-lookup"><span data-stu-id="d0d04-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="d0d04-109">이 명령은 리포지토리의 지정된 분기에 현재 구성 스냅숏을 사용하여 커밋을 만들어 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="d0d04-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0d04-110">PARAMETERS</span></span>

### <span data-ttu-id="d0d04-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="d0d04-111">-Branch</span></span>
<span data-ttu-id="d0d04-112">현재 구성 스냅숏을 커밋할 Git 분기의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="d0d04-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d0d04-113">-Context</span></span>
<span data-ttu-id="d0d04-114">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="d0d04-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d0d04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d04-115">-DefaultProfile</span></span>
<span data-ttu-id="d0d04-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0d04-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d0d04-117">-Force</span></span>
<span data-ttu-id="d0d04-118">이 cmdlet은 Git 리포지토리에 덮어 새 변경 내용이 있는 경우에도 현재 구성 데이터베이스를 Git 리포지토리에 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="d0d04-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0d04-119">-PassThru</span></span>
<span data-ttu-id="d0d04-120">이 cmdlet은 **PsApiManagementOperationResult 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="d0d04-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="d0d04-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d0d04-121">-Confirm</span></span>
<span data-ttu-id="d0d04-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0d04-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0d04-123">-WhatIf</span></span>
<span data-ttu-id="d0d04-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0d04-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0d04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d04-126">CommonParameters</span></span>
<span data-ttu-id="d0d04-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0d04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d04-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0d04-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d04-129">입력</span><span class="sxs-lookup"><span data-stu-id="d0d04-129">INPUTS</span></span>

### <span data-ttu-id="d0d04-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d0d04-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0d04-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d0d04-131">System.String</span></span>

### <span data-ttu-id="d0d04-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d0d04-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0d04-133">출력</span><span class="sxs-lookup"><span data-stu-id="d0d04-133">OUTPUTS</span></span>

### <span data-ttu-id="d0d04-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="d0d04-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="d0d04-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0d04-135">NOTES</span></span>

## <span data-ttu-id="d0d04-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0d04-136">RELATED LINKS</span></span>

[<span data-ttu-id="d0d04-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0d04-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


