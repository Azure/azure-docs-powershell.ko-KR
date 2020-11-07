---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873859"
---
# <span data-ttu-id="51585-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="51585-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="51585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51585-102">SYNOPSIS</span></span>
<span data-ttu-id="51585-103">인스턴스 장애 조치 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51585-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="51585-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51585-104">SYNTAX</span></span>

### <span data-ttu-id="51585-105">RemoveIFGDefault (기본값)</span><span class="sxs-lookup"><span data-stu-id="51585-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51585-106">리소스 Id에서 인스턴스 장애 조치 (Failover) 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="51585-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51585-107">AzureSqlInstanceFailoverGroupModel 인스턴스 정의에서 인스턴스 장애 조치 (Failover) 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="51585-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51585-108">설명은</span><span class="sxs-lookup"><span data-stu-id="51585-108">DESCRIPTION</span></span>
<span data-ttu-id="51585-109">이 명령은 지정 된 이름의 인스턴스 장애 조치 (Failover) 그룹을 제거 하 고 모든 데이터베이스는 그대로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="51585-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="51585-110">수신기 끝점은 DNS에서 등록 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51585-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="51585-111">명령을 실행 하려면 인스턴스 장애 조치 그룹의 기본 영역을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51585-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="51585-112">예제의</span><span class="sxs-lookup"><span data-stu-id="51585-112">EXAMPLES</span></span>

### <span data-ttu-id="51585-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="51585-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="51585-114">인스턴스 장애 조치 (Failover) 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51585-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="51585-115">변수</span><span class="sxs-lookup"><span data-stu-id="51585-115">PARAMETERS</span></span>

### <span data-ttu-id="51585-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51585-116">-DefaultProfile</span></span>
<span data-ttu-id="51585-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51585-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51585-118">-Force</span><span class="sxs-lookup"><span data-stu-id="51585-118">-Force</span></span>
<span data-ttu-id="51585-119">작업 수행에 대 한 건너뛰기 확인 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="51585-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="51585-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51585-120">-InputObject</span></span>
<span data-ttu-id="51585-121">제거할 인스턴스 장애 조치 (Failover) 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="51585-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51585-122">-위치</span><span class="sxs-lookup"><span data-stu-id="51585-122">-Location</span></span>
<span data-ttu-id="51585-123">인스턴스 장애 조치 (Failover) 그룹을 검색할 로컬 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51585-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51585-124">-이름</span><span class="sxs-lookup"><span data-stu-id="51585-124">-Name</span></span>
<span data-ttu-id="51585-125">제거할 인스턴스 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51585-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51585-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51585-126">-ResourceGroupName</span></span>
<span data-ttu-id="51585-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51585-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51585-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51585-128">-ResourceId</span></span>
<span data-ttu-id="51585-129">제거할 인스턴스 장애 조치 (Failover) 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="51585-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51585-130">-확인</span><span class="sxs-lookup"><span data-stu-id="51585-130">-Confirm</span></span>
<span data-ttu-id="51585-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51585-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51585-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51585-132">-WhatIf</span></span>
<span data-ttu-id="51585-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51585-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51585-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51585-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51585-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51585-135">CommonParameters</span></span>
<span data-ttu-id="51585-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51585-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51585-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51585-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51585-138">입력</span><span class="sxs-lookup"><span data-stu-id="51585-138">INPUTS</span></span>

### <span data-ttu-id="51585-139">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="51585-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="51585-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="51585-140">System.String</span></span>

## <span data-ttu-id="51585-141">출력</span><span class="sxs-lookup"><span data-stu-id="51585-141">OUTPUTS</span></span>

### <span data-ttu-id="51585-142">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="51585-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="51585-143">상속자</span><span class="sxs-lookup"><span data-stu-id="51585-143">NOTES</span></span>

## <span data-ttu-id="51585-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51585-144">RELATED LINKS</span></span>
