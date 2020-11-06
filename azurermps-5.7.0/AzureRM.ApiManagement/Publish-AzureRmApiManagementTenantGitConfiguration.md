---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529947"
---
# <span data-ttu-id="94039-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="94039-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="94039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94039-102">SYNOPSIS</span></span>
<span data-ttu-id="94039-103">Git 분기의 변경 내용을 구성 데이터베이스에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94039-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94039-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94039-105">설명은</span><span class="sxs-lookup"><span data-stu-id="94039-105">DESCRIPTION</span></span>
<span data-ttu-id="94039-106">**AzureRmApiManagementTenantGitConfiguration** Cmdlet은 Git 분기의 변경 내용을 구성 데이터베이스에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="94039-107">또는 게시 하지 않고 Git 분기의 변경 내용에 대 한 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="94039-108">예제의</span><span class="sxs-lookup"><span data-stu-id="94039-108">EXAMPLES</span></span>

### <span data-ttu-id="94039-109">예제 1: Git 변경 내용 배포</span><span class="sxs-lookup"><span data-stu-id="94039-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="94039-110">이 명령은 지정 된 분기의 변경 내용을 구성 데이터베이스에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="94039-111">예제 2: Git 변경 내용 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="94039-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="94039-112">이 명령은 구성 데이터베이스에 대해 Git 분기의 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="94039-113">변경 내용이 게시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-113">It does not publish changes.</span></span>

## <span data-ttu-id="94039-114">변수</span><span class="sxs-lookup"><span data-stu-id="94039-114">PARAMETERS</span></span>

### <span data-ttu-id="94039-115">-분기</span><span class="sxs-lookup"><span data-stu-id="94039-115">-Branch</span></span>
<span data-ttu-id="94039-116">이 cmdlet이 구성을 구성 데이터베이스에 배포 하는 Git 분기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="94039-117">-Context</span></span>
<span data-ttu-id="94039-118">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94039-119">-DefaultProfile</span></span>
<span data-ttu-id="94039-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94039-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94039-121">-Force</span><span class="sxs-lookup"><span data-stu-id="94039-121">-Force</span></span>
<span data-ttu-id="94039-122">이 cmdlet이이 업데이트에서 삭제 되는 제품에 대 한 구독을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94039-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94039-123">-PassThru</span></span>
<span data-ttu-id="94039-124">이 cmdlet이 **PsApiManagementOperationResult** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94039-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="94039-125">-ValidateOnly</span></span>
<span data-ttu-id="94039-126">이 cmdlet이 지정 된 Git 분기의 변경 내용에 대 한 유효성 검사를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94039-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="94039-127">구성 데이터베이스에 게시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-127">It does not publish to the configuration database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94039-128">-확인</span><span class="sxs-lookup"><span data-stu-id="94039-128">-Confirm</span></span>
<span data-ttu-id="94039-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94039-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94039-130">-WhatIf</span></span>
<span data-ttu-id="94039-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94039-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94039-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94039-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94039-133">CommonParameters</span></span>
<span data-ttu-id="94039-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94039-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94039-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94039-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94039-136">입력</span><span class="sxs-lookup"><span data-stu-id="94039-136">INPUTS</span></span>

### <span data-ttu-id="94039-137">않아야</span><span class="sxs-lookup"><span data-stu-id="94039-137">None</span></span>
<span data-ttu-id="94039-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94039-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94039-139">출력</span><span class="sxs-lookup"><span data-stu-id="94039-139">OUTPUTS</span></span>

### <span data-ttu-id="94039-140">ApiManagement. ServiceManagement. \ PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="94039-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="94039-141">상속자</span><span class="sxs-lookup"><span data-stu-id="94039-141">NOTES</span></span>

## <span data-ttu-id="94039-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94039-142">RELATED LINKS</span></span>

[<span data-ttu-id="94039-143">저장-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="94039-143">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


