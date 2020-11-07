---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: 97f6417bf2d58009e7a656dca280db4be2994879
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873574"
---
# <span data-ttu-id="bf0e5-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="bf0e5-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="bf0e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0e5-103">Azure SQL 인스턴스 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="bf0e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf0e5-104">SYNTAX</span></span>

### <span data-ttu-id="bf0e5-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bf0e5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0e5-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf0e5-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0e5-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf0e5-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf0e5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bf0e5-108">DESCRIPTION</span></span>
<span data-ttu-id="bf0e5-109">**AzSqlInstancePool** Cmdlet은 Azure SQL 인스턴스 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="bf0e5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bf0e5-110">EXAMPLES</span></span>

### <span data-ttu-id="bf0e5-111">예제 1: 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="bf0e5-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="bf0e5-112">예제 2: 리소스 식별자를 기준으로 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="bf0e5-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="bf0e5-113">예제 3: 인스턴스 풀 개체를 기준으로 인스턴스 풀 제거</span><span class="sxs-lookup"><span data-stu-id="bf0e5-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="bf0e5-114">이 명령은 instancePool0 이라는 인스턴스 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="bf0e5-115">변수</span><span class="sxs-lookup"><span data-stu-id="bf0e5-115">PARAMETERS</span></span>

### <span data-ttu-id="bf0e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0e5-116">-DefaultProfile</span></span>
<span data-ttu-id="bf0e5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0e5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf0e5-118">-InputObject</span></span>
<span data-ttu-id="bf0e5-119">제거할 인스턴스 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e5-120">-이름</span><span class="sxs-lookup"><span data-stu-id="bf0e5-120">-Name</span></span>
<span data-ttu-id="bf0e5-121">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf0e5-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf0e5-124">-ResourceId</span></span>
<span data-ttu-id="bf0e5-125">제거할 인스턴스 풀 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0e5-126">-확인</span><span class="sxs-lookup"><span data-stu-id="bf0e5-126">-Confirm</span></span>
<span data-ttu-id="bf0e5-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf0e5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0e5-128">-WhatIf</span></span>
<span data-ttu-id="bf0e5-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf0e5-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf0e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0e5-131">CommonParameters</span></span>
<span data-ttu-id="bf0e5-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0e5-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0e5-134">입력</span><span class="sxs-lookup"><span data-stu-id="bf0e5-134">INPUTS</span></span>

### <span data-ttu-id="bf0e5-135">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="bf0e5-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="bf0e5-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf0e5-136">System.String</span></span>

## <span data-ttu-id="bf0e5-137">출력</span><span class="sxs-lookup"><span data-stu-id="bf0e5-137">OUTPUTS</span></span>

### <span data-ttu-id="bf0e5-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="bf0e5-138">System.Object</span></span>
## <span data-ttu-id="bf0e5-139">상속자</span><span class="sxs-lookup"><span data-stu-id="bf0e5-139">NOTES</span></span>

## <span data-ttu-id="bf0e5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf0e5-140">RELATED LINKS</span></span>
