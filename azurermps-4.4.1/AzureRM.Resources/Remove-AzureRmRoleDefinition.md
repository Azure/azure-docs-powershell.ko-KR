---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703321"
---
# <span data-ttu-id="b1664-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b1664-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="b1664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1664-102">SYNOPSIS</span></span>
<span data-ttu-id="b1664-103">Azure RBAC에서 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b1664-104">삭제할 역할은 역할의 Id 속성을 사용 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="b1664-105">사용자 지정 역할에 대 한 기존 역할 할당이 있으면 Delete가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1664-106">구문과</span><span class="sxs-lookup"><span data-stu-id="b1664-106">SYNTAX</span></span>

### <span data-ttu-id="b1664-107">RoleDefinitionIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1664-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1664-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1664-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1664-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b1664-109">DESCRIPTION</span></span>
<span data-ttu-id="b1664-110">Remove-AzureRmRoleDefinition cmdlet은 Azure Role-Based 액세스 제어에서 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b1664-111">기존 사용자 지정 역할의 Id 매개 변수를 제공 하 여 해당 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="b1664-112">기본적으로 Remove-AzureRmRoleDefinition 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="b1664-113">프롬프트를 표시 하지 않으려면 Force 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="b1664-114">사용자 지정 역할에 대해 삭제 될 기존 역할 할당이 있는 경우 삭제는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="b1664-115">예제의</span><span class="sxs-lookup"><span data-stu-id="b1664-115">EXAMPLES</span></span>

### <span data-ttu-id="b1664-116">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1664-116">--------------------------  Example 1  --------------------------</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="b1664-117">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1664-117">--------------------------  Example 2  --------------------------</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="b1664-118">변수</span><span class="sxs-lookup"><span data-stu-id="b1664-118">PARAMETERS</span></span>

### <span data-ttu-id="b1664-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b1664-119">-Force</span></span>
<span data-ttu-id="b1664-120">설정 하는 경우 사용자 지정 역할을 삭제 하기 전에 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-120">If set, does not prompt for a confirmation before deleting the custom role</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1664-121">-Id</span><span class="sxs-lookup"><span data-stu-id="b1664-121">-Id</span></span>
<span data-ttu-id="b1664-122">삭제할 역할 정의의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-122">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1664-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b1664-123">-Name</span></span>
<span data-ttu-id="b1664-124">삭제할 역할 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-124">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1664-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1664-125">-PassThru</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1664-126">-범위</span><span class="sxs-lookup"><span data-stu-id="b1664-126">-Scope</span></span>
<span data-ttu-id="b1664-127">역할 정의 범위</span><span class="sxs-lookup"><span data-stu-id="b1664-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1664-128">-확인</span><span class="sxs-lookup"><span data-stu-id="b1664-128">-Confirm</span></span>
<span data-ttu-id="b1664-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1664-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1664-130">-WhatIf</span></span>
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

### <span data-ttu-id="b1664-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1664-131">-DefaultProfile</span></span>
<span data-ttu-id="b1664-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1664-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1664-133">CommonParameters</span></span>
<span data-ttu-id="b1664-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1664-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1664-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1664-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1664-136">입력</span><span class="sxs-lookup"><span data-stu-id="b1664-136">INPUTS</span></span>

## <span data-ttu-id="b1664-137">출력</span><span class="sxs-lookup"><span data-stu-id="b1664-137">OUTPUTS</span></span>

### <span data-ttu-id="b1664-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b1664-138">System.Boolean</span></span>

## <span data-ttu-id="b1664-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b1664-139">NOTES</span></span>
<span data-ttu-id="b1664-140">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="b1664-140">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b1664-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1664-141">RELATED LINKS</span></span>

[<span data-ttu-id="b1664-142">새로운 AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b1664-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="b1664-143">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b1664-143">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="b1664-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b1664-144">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

