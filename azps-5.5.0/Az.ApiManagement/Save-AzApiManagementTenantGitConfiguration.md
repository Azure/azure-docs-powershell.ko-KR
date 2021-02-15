---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182340"
---
# <span data-ttu-id="d1b7a-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1b7a-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="d1b7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b7a-103">현재 구성에 대한 커밋을 만들어 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="d1b7a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1b7a-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1b7a-105">설명</span><span class="sxs-lookup"><span data-stu-id="d1b7a-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b7a-106">**Save-AzApiManagementTenantGitConfiguration** cmdlet은 리포지토리의 분기에 현재 구성 스냅숏을 포함하는 커밋을 만들어 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="d1b7a-107">예제</span><span class="sxs-lookup"><span data-stu-id="d1b7a-107">EXAMPLES</span></span>

### <span data-ttu-id="d1b7a-108">예제 1: 구성에 변경 내용 저장</span><span class="sxs-lookup"><span data-stu-id="d1b7a-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="d1b7a-109">이 명령은 현재 구성 스냅숏을 사용하여 리포지토리의 지정된 분기에 커밋을 만들어 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="d1b7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1b7a-110">PARAMETERS</span></span>

### <span data-ttu-id="d1b7a-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="d1b7a-111">-Branch</span></span>
<span data-ttu-id="d1b7a-112">현재 구성 스냅숏을 커밋할 Git 분기의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="d1b7a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d1b7a-113">-Context</span></span>
<span data-ttu-id="d1b7a-114">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="d1b7a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d1b7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b7a-115">-DefaultProfile</span></span>
<span data-ttu-id="d1b7a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1b7a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d1b7a-117">-Force</span></span>
<span data-ttu-id="d1b7a-118">이 cmdlet이 현재 구성 데이터베이스를 Git 리포지토리에 커밋하는지 지정합니다. Git 리포지토리에 덮어 덮어입은 새로운 변경 내용이 있는 경우에도 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="d1b7a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1b7a-119">-PassThru</span></span>
<span data-ttu-id="d1b7a-120">이 cmdlet이 **PsApiManagementOperationResult 개체를 반환하는지 나타냅니다.**</span><span class="sxs-lookup"><span data-stu-id="d1b7a-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="d1b7a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1b7a-121">-Confirm</span></span>
<span data-ttu-id="d1b7a-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b7a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b7a-123">-WhatIf</span></span>
<span data-ttu-id="d1b7a-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d1b7a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1b7a-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b7a-126">CommonParameters</span></span>
<span data-ttu-id="d1b7a-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b7a-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1b7a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b7a-129">입력</span><span class="sxs-lookup"><span data-stu-id="d1b7a-129">INPUTS</span></span>

### <span data-ttu-id="d1b7a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1b7a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1b7a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d1b7a-131">System.String</span></span>

### <span data-ttu-id="d1b7a-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1b7a-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1b7a-133">출력</span><span class="sxs-lookup"><span data-stu-id="d1b7a-133">OUTPUTS</span></span>

### <span data-ttu-id="d1b7a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="d1b7a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="d1b7a-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1b7a-135">NOTES</span></span>

## <span data-ttu-id="d1b7a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1b7a-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1b7a-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1b7a-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


