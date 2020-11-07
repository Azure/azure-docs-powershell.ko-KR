---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1986a773a61f9c0ac1bd9a30992db3843b97e438
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873583"
---
# <span data-ttu-id="e21d6-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="e21d6-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="e21d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e21d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e21d6-103">탄력적 작업 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21d6-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="e21d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e21d6-104">SYNTAX</span></span>

### <span data-ttu-id="e21d6-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e21d6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21d6-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="e21d6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21d6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e21d6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e21d6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e21d6-108">DESCRIPTION</span></span>
<span data-ttu-id="e21d6-109">Remove-AzSqlElasticJobCredential cmdlet은 작업 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21d6-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="e21d6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e21d6-110">EXAMPLES</span></span>

### <span data-ttu-id="e21d6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e21d6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="e21d6-112">작업 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="e21d6-112">Removes a job credential</span></span>

## <span data-ttu-id="e21d6-113">변수</span><span class="sxs-lookup"><span data-stu-id="e21d6-113">PARAMETERS</span></span>

### <span data-ttu-id="e21d6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e21d6-114">-AgentName</span></span>
<span data-ttu-id="e21d6-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="e21d6-115">The agent name</span></span>

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

### <span data-ttu-id="e21d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21d6-116">-DefaultProfile</span></span>
<span data-ttu-id="e21d6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e21d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21d6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e21d6-118">-InputObject</span></span>
<span data-ttu-id="e21d6-119">작업 자격 증명 개체</span><span class="sxs-lookup"><span data-stu-id="e21d6-119">The job credential object</span></span>

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

### <span data-ttu-id="e21d6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e21d6-120">-Name</span></span>
<span data-ttu-id="e21d6-121">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="e21d6-121">The job credential name</span></span>

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

### <span data-ttu-id="e21d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="e21d6-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e21d6-123">The resource group name</span></span>

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

### <span data-ttu-id="e21d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e21d6-124">-ResourceId</span></span>
<span data-ttu-id="e21d6-125">작업 자격 증명 리소스 id</span><span class="sxs-lookup"><span data-stu-id="e21d6-125">The job credential resource id</span></span>

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

### <span data-ttu-id="e21d6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e21d6-126">-ServerName</span></span>
<span data-ttu-id="e21d6-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="e21d6-127">The server name</span></span>

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

### <span data-ttu-id="e21d6-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e21d6-128">-Confirm</span></span>
<span data-ttu-id="e21d6-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e21d6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e21d6-130">-WhatIf</span></span>
<span data-ttu-id="e21d6-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e21d6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e21d6-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e21d6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e21d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21d6-133">CommonParameters</span></span>
<span data-ttu-id="e21d6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21d6-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e21d6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21d6-136">입력</span><span class="sxs-lookup"><span data-stu-id="e21d6-136">INPUTS</span></span>

### <span data-ttu-id="e21d6-137">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e21d6-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="e21d6-138">출력</span><span class="sxs-lookup"><span data-stu-id="e21d6-138">OUTPUTS</span></span>

### <span data-ttu-id="e21d6-139">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e21d6-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="e21d6-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e21d6-140">NOTES</span></span>

## <span data-ttu-id="e21d6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e21d6-141">RELATED LINKS</span></span>
