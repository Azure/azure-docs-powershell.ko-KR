---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 2a867109bf44cd652eaf1d256d963796e06762cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527748"
---
# <span data-ttu-id="ecb6c-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb6c-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="ecb6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb6c-103">Git 분기의 변경 내용을 구성 데이터베이스에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecb6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecb6c-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecb6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecb6c-105">DESCRIPTION</span></span>
<span data-ttu-id="ecb6c-106">**AzureRmApiManagementTenantGitConfiguration** Cmdlet은 Git 분기의 변경 내용을 구성 데이터베이스에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="ecb6c-107">또는 게시 하지 않고 Git 분기의 변경 내용에 대 한 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="ecb6c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ecb6c-108">EXAMPLES</span></span>

### <span data-ttu-id="ecb6c-109">예제 1: Git 변경 내용 배포</span><span class="sxs-lookup"><span data-stu-id="ecb6c-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="ecb6c-110">이 명령은 지정 된 분기의 변경 내용을 구성 데이터베이스에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="ecb6c-111">예제 2: Git 변경 내용 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="ecb6c-111">Example 2: Validate Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="ecb6c-112">이 명령은 구성 데이터베이스에 대해 Git 분기의 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="ecb6c-113">변경 내용이 게시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-113">It does not publish changes.</span></span>

## <span data-ttu-id="ecb6c-114">변수</span><span class="sxs-lookup"><span data-stu-id="ecb6c-114">PARAMETERS</span></span>

### <span data-ttu-id="ecb6c-115">-분기</span><span class="sxs-lookup"><span data-stu-id="ecb6c-115">-Branch</span></span>
<span data-ttu-id="ecb6c-116">이 cmdlet이 구성을 구성 데이터베이스에 배포 하는 Git 분기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="ecb6c-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ecb6c-117">-Context</span></span>
<span data-ttu-id="ecb6c-118">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ecb6c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ecb6c-119">-Force</span></span>
<span data-ttu-id="ecb6c-120">이 cmdlet이이 업데이트에서 삭제 되는 제품에 대 한 구독을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-120">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="ecb6c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecb6c-121">-PassThru</span></span>
<span data-ttu-id="ecb6c-122">이 cmdlet이 **PsApiManagementOperationResult** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-122">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="ecb6c-123">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ecb6c-123">-ValidateOnly</span></span>
<span data-ttu-id="ecb6c-124">이 cmdlet이 지정 된 Git 분기의 변경 내용에 대 한 유효성 검사를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-124">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="ecb6c-125">구성 데이터베이스에 게시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-125">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="ecb6c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="ecb6c-126">-Confirm</span></span>
<span data-ttu-id="ecb6c-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb6c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb6c-128">-WhatIf</span></span>
<span data-ttu-id="ecb6c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb6c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb6c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb6c-131">-DefaultProfile</span></span>
<span data-ttu-id="ecb6c-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb6c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb6c-133">CommonParameters</span></span>
<span data-ttu-id="ecb6c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb6c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb6c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb6c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb6c-136">입력</span><span class="sxs-lookup"><span data-stu-id="ecb6c-136">INPUTS</span></span>

## <span data-ttu-id="ecb6c-137">출력</span><span class="sxs-lookup"><span data-stu-id="ecb6c-137">OUTPUTS</span></span>

### <span data-ttu-id="ecb6c-138">ApiManagement. ServiceManagement. \ PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="ecb6c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="ecb6c-139">상속자</span><span class="sxs-lookup"><span data-stu-id="ecb6c-139">NOTES</span></span>

## <span data-ttu-id="ecb6c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb6c-140">RELATED LINKS</span></span>

[<span data-ttu-id="ecb6c-141">저장-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecb6c-141">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


