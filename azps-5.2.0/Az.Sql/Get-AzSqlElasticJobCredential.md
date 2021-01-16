---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346533"
---
# <span data-ttu-id="a9e88-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="a9e88-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="a9e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e88-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e88-103">하나 이상의 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e88-103">Gets one or more credentials</span></span>

## <span data-ttu-id="a9e88-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9e88-104">SYNTAX</span></span>

### <span data-ttu-id="a9e88-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a9e88-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e88-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9e88-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e88-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9e88-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9e88-108">설명</span><span class="sxs-lookup"><span data-stu-id="a9e88-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e88-109">Get-AzSqlElasticJobCredential cmdlet은 하나 이상의 작업 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e88-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="a9e88-110">예제</span><span class="sxs-lookup"><span data-stu-id="a9e88-110">EXAMPLES</span></span>

### <span data-ttu-id="a9e88-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9e88-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="a9e88-112">작업 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e88-112">Gets a job credential</span></span>

## <span data-ttu-id="a9e88-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9e88-113">PARAMETERS</span></span>

### <span data-ttu-id="a9e88-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a9e88-114">-AgentName</span></span>
<span data-ttu-id="a9e88-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="a9e88-115">The agent name</span></span>

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

### <span data-ttu-id="a9e88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e88-116">-DefaultProfile</span></span>
<span data-ttu-id="a9e88-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e88-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e88-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a9e88-118">-Name</span></span>
<span data-ttu-id="a9e88-119">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="a9e88-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9e88-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a9e88-120">-ParentObject</span></span>
<span data-ttu-id="a9e88-121">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="a9e88-121">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e88-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e88-122">-ParentResourceId</span></span>
<span data-ttu-id="a9e88-123">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a9e88-123">The agent resource id</span></span>

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

### <span data-ttu-id="a9e88-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e88-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9e88-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a9e88-125">The resource group name</span></span>

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

### <span data-ttu-id="a9e88-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9e88-126">-ServerName</span></span>
<span data-ttu-id="a9e88-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="a9e88-127">The server name</span></span>

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

### <span data-ttu-id="a9e88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e88-128">CommonParameters</span></span>
<span data-ttu-id="a9e88-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e88-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9e88-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e88-131">입력</span><span class="sxs-lookup"><span data-stu-id="a9e88-131">INPUTS</span></span>

### <span data-ttu-id="a9e88-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a9e88-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a9e88-133">출력</span><span class="sxs-lookup"><span data-stu-id="a9e88-133">OUTPUTS</span></span>

### <span data-ttu-id="a9e88-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="a9e88-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="a9e88-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9e88-135">NOTES</span></span>

## <span data-ttu-id="a9e88-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9e88-136">RELATED LINKS</span></span>
