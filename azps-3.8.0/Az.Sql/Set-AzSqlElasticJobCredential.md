---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878830"
---
# <span data-ttu-id="400df-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="400df-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="400df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="400df-102">SYNOPSIS</span></span>
<span data-ttu-id="400df-103">작업 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="400df-103">Updates a job credential</span></span>

## <span data-ttu-id="400df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="400df-104">SYNTAX</span></span>

### <span data-ttu-id="400df-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="400df-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="400df-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="400df-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="400df-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="400df-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="400df-108">설명은</span><span class="sxs-lookup"><span data-stu-id="400df-108">DESCRIPTION</span></span>
<span data-ttu-id="400df-109">Set-AzSqlElasticJobCredential cmdlet이 작업 자격 증명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="400df-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="400df-110">예제의</span><span class="sxs-lookup"><span data-stu-id="400df-110">EXAMPLES</span></span>

### <span data-ttu-id="400df-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="400df-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="400df-112">작업 자격 증명 업데이트</span><span class="sxs-lookup"><span data-stu-id="400df-112">Updates a job credential</span></span>

## <span data-ttu-id="400df-113">변수</span><span class="sxs-lookup"><span data-stu-id="400df-113">PARAMETERS</span></span>

### <span data-ttu-id="400df-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="400df-114">-AgentName</span></span>
<span data-ttu-id="400df-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="400df-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400df-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="400df-116">-Credential</span></span>
<span data-ttu-id="400df-117">자격 증명</span><span class="sxs-lookup"><span data-stu-id="400df-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="400df-118">-DefaultProfile</span></span>
<span data-ttu-id="400df-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="400df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="400df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="400df-120">-InputObject</span></span>
<span data-ttu-id="400df-121">작업 자격 증명 개체</span><span class="sxs-lookup"><span data-stu-id="400df-121">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="400df-122">-이름</span><span class="sxs-lookup"><span data-stu-id="400df-122">-Name</span></span>
<span data-ttu-id="400df-123">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="400df-123">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="400df-124">-ResourceGroupName</span></span>
<span data-ttu-id="400df-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="400df-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400df-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="400df-126">-ResourceId</span></span>
<span data-ttu-id="400df-127">작업 자격 증명 리소스 id</span><span class="sxs-lookup"><span data-stu-id="400df-127">The job credential resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="400df-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="400df-128">-ServerName</span></span>
<span data-ttu-id="400df-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="400df-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400df-130">-확인</span><span class="sxs-lookup"><span data-stu-id="400df-130">-Confirm</span></span>
<span data-ttu-id="400df-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="400df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="400df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="400df-132">-WhatIf</span></span>
<span data-ttu-id="400df-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="400df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="400df-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="400df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="400df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="400df-135">CommonParameters</span></span>
<span data-ttu-id="400df-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="400df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="400df-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="400df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="400df-138">입력</span><span class="sxs-lookup"><span data-stu-id="400df-138">INPUTS</span></span>

### <span data-ttu-id="400df-139">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="400df-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="400df-140">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="400df-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="400df-141">출력</span><span class="sxs-lookup"><span data-stu-id="400df-141">OUTPUTS</span></span>

### <span data-ttu-id="400df-142">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="400df-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="400df-143">상속자</span><span class="sxs-lookup"><span data-stu-id="400df-143">NOTES</span></span>

## <span data-ttu-id="400df-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="400df-144">RELATED LINKS</span></span>
