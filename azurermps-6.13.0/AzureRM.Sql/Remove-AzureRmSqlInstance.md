---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534192"
---
# <span data-ttu-id="2fc21-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2fc21-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="2fc21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc21-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc21-103">Azure SQL 관리 데이터베이스 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fc21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fc21-104">SYNTAX</span></span>

### <span data-ttu-id="2fc21-105">RemoveInstanceFromInputParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="2fc21-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc21-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="2fc21-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc21-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc21-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc21-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2fc21-108">DESCRIPTION</span></span>
<span data-ttu-id="2fc21-109">**AzureRmSqlInstance** Cmdlet은 Azure SQL Database 관리 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="2fc21-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2fc21-110">EXAMPLES</span></span>

### <span data-ttu-id="2fc21-111">예제 1: 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="2fc21-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2fc21-112">이 명령은 managedInstance1 이라는 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="2fc21-113">변수</span><span class="sxs-lookup"><span data-stu-id="2fc21-113">PARAMETERS</span></span>

### <span data-ttu-id="2fc21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc21-114">-DefaultProfile</span></span>
<span data-ttu-id="2fc21-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc21-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2fc21-116">-Force</span></span>
<span data-ttu-id="2fc21-117">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="2fc21-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc21-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc21-118">-InputObject</span></span>
<span data-ttu-id="2fc21-119">제거할 AzureSqlManagedInstanceModel 개체</span><span class="sxs-lookup"><span data-stu-id="2fc21-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc21-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2fc21-120">-Name</span></span>
<span data-ttu-id="2fc21-121">SQL 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc21-122">-ResourceGroupName</span></span>
<span data-ttu-id="2fc21-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc21-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc21-124">-ResourceId</span></span>
<span data-ttu-id="2fc21-125">제거할 인스턴스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc21-126">-확인</span><span class="sxs-lookup"><span data-stu-id="2fc21-126">-Confirm</span></span>
<span data-ttu-id="2fc21-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc21-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc21-128">-WhatIf</span></span>
<span data-ttu-id="2fc21-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc21-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc21-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc21-131">CommonParameters</span></span>
<span data-ttu-id="2fc21-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc21-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc21-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc21-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc21-134">입력</span><span class="sxs-lookup"><span data-stu-id="2fc21-134">INPUTS</span></span>

### <span data-ttu-id="2fc21-135">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="2fc21-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="2fc21-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2fc21-136">System.String</span></span>

## <span data-ttu-id="2fc21-137">출력</span><span class="sxs-lookup"><span data-stu-id="2fc21-137">OUTPUTS</span></span>

### <span data-ttu-id="2fc21-138">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="2fc21-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="2fc21-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2fc21-139">NOTES</span></span>

## <span data-ttu-id="2fc21-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fc21-140">RELATED LINKS</span></span>
