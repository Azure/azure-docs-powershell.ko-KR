---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 13878e7ca0ea4ed0b03734f0395c9f819e04d7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873673"
---
# <span data-ttu-id="00c00-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="00c00-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="00c00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00c00-102">SYNOPSIS</span></span>
<span data-ttu-id="00c00-103">하나 이상의 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00c00-103">Gets one or more credentials</span></span>

## <span data-ttu-id="00c00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00c00-104">SYNTAX</span></span>

### <span data-ttu-id="00c00-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="00c00-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00c00-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="00c00-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00c00-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="00c00-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00c00-108">설명은</span><span class="sxs-lookup"><span data-stu-id="00c00-108">DESCRIPTION</span></span>
<span data-ttu-id="00c00-109">Get-AzSqlElasticJobCredential cmdlet은 하나 이상의 작업 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00c00-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="00c00-110">예제의</span><span class="sxs-lookup"><span data-stu-id="00c00-110">EXAMPLES</span></span>

### <span data-ttu-id="00c00-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="00c00-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="00c00-112">작업 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00c00-112">Gets a job credential</span></span>

## <span data-ttu-id="00c00-113">변수</span><span class="sxs-lookup"><span data-stu-id="00c00-113">PARAMETERS</span></span>

### <span data-ttu-id="00c00-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="00c00-114">-AgentName</span></span>
<span data-ttu-id="00c00-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="00c00-115">The agent name</span></span>

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

### <span data-ttu-id="00c00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c00-116">-DefaultProfile</span></span>
<span data-ttu-id="00c00-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00c00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00c00-118">-이름</span><span class="sxs-lookup"><span data-stu-id="00c00-118">-Name</span></span>
<span data-ttu-id="00c00-119">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="00c00-119">The job credential name</span></span>

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

### <span data-ttu-id="00c00-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="00c00-120">-ParentObject</span></span>
<span data-ttu-id="00c00-121">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="00c00-121">The agent object</span></span>

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

### <span data-ttu-id="00c00-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="00c00-122">-ParentResourceId</span></span>
<span data-ttu-id="00c00-123">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="00c00-123">The agent resource id</span></span>

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

### <span data-ttu-id="00c00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c00-124">-ResourceGroupName</span></span>
<span data-ttu-id="00c00-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="00c00-125">The resource group name</span></span>

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

### <span data-ttu-id="00c00-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="00c00-126">-ServerName</span></span>
<span data-ttu-id="00c00-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="00c00-127">The server name</span></span>

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

### <span data-ttu-id="00c00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c00-128">CommonParameters</span></span>
<span data-ttu-id="00c00-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00c00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c00-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00c00-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c00-131">입력</span><span class="sxs-lookup"><span data-stu-id="00c00-131">INPUTS</span></span>

### <span data-ttu-id="00c00-132">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="00c00-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="00c00-133">출력</span><span class="sxs-lookup"><span data-stu-id="00c00-133">OUTPUTS</span></span>

### <span data-ttu-id="00c00-134">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="00c00-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="00c00-135">상속자</span><span class="sxs-lookup"><span data-stu-id="00c00-135">NOTES</span></span>

## <span data-ttu-id="00c00-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00c00-136">RELATED LINKS</span></span>
