---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b4abd2d8dab9e4c41d2e42be77bee62428ccc712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869381"
---
# <span data-ttu-id="26092-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="26092-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="26092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26092-102">SYNOPSIS</span></span>
<span data-ttu-id="26092-103">현재 구성에 대 한 커밋을 만들어 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="26092-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26092-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26092-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26092-105">DESCRIPTION</span></span>
<span data-ttu-id="26092-106">**AzApiManagementTenantGitConfiguration** cmdlet은 현재 구성 스냅숏이 저장소의 분기에 포함 된 커밋을 만들어 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="26092-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26092-107">EXAMPLES</span></span>

### <span data-ttu-id="26092-108">예제 1: 구성 변경 내용 저장</span><span class="sxs-lookup"><span data-stu-id="26092-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="26092-109">이 명령은 현재 구성 스냅샷이 저장소의 지정 된 분기에 대 한 커밋을 만들어 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="26092-110">변수</span><span class="sxs-lookup"><span data-stu-id="26092-110">PARAMETERS</span></span>

### <span data-ttu-id="26092-111">-분기</span><span class="sxs-lookup"><span data-stu-id="26092-111">-Branch</span></span>
<span data-ttu-id="26092-112">현재 구성 스냅숏을 커밋할 Git 분기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="26092-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="26092-113">-Context</span></span>
<span data-ttu-id="26092-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="26092-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26092-115">-DefaultProfile</span></span>
<span data-ttu-id="26092-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26092-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26092-117">-Force</span><span class="sxs-lookup"><span data-stu-id="26092-117">-Force</span></span>
<span data-ttu-id="26092-118">Git 리포지토리에서 덮어쓴 새 변경 내용이 포함 된 경우에도이 cmdlet이 현재 구성 데이터베이스를 Git 리포지토리에 커밋 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="26092-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26092-119">-PassThru</span></span>
<span data-ttu-id="26092-120">이 cmdlet이 **PsApiManagementOperationResult** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="26092-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="26092-121">-확인</span><span class="sxs-lookup"><span data-stu-id="26092-121">-Confirm</span></span>
<span data-ttu-id="26092-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26092-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26092-123">-WhatIf</span></span>
<span data-ttu-id="26092-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26092-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26092-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26092-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26092-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26092-126">CommonParameters</span></span>
<span data-ttu-id="26092-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26092-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26092-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26092-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26092-129">입력</span><span class="sxs-lookup"><span data-stu-id="26092-129">INPUTS</span></span>

### <span data-ttu-id="26092-130">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26092-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26092-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26092-131">System.String</span></span>

### <span data-ttu-id="26092-132">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="26092-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26092-133">출력</span><span class="sxs-lookup"><span data-stu-id="26092-133">OUTPUTS</span></span>

### <span data-ttu-id="26092-134">ApiManagement. ServiceManagement. \ PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="26092-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="26092-135">상속자</span><span class="sxs-lookup"><span data-stu-id="26092-135">NOTES</span></span>

## <span data-ttu-id="26092-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26092-136">RELATED LINKS</span></span>

[<span data-ttu-id="26092-137">게시-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="26092-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


