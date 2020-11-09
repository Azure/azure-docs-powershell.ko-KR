---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308222"
---
# <span data-ttu-id="5173f-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="5173f-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="5173f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5173f-102">SYNOPSIS</span></span>
<span data-ttu-id="5173f-103">탄력적 작업 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5173f-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="5173f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5173f-104">SYNTAX</span></span>

### <span data-ttu-id="5173f-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5173f-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5173f-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="5173f-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5173f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5173f-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5173f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5173f-108">DESCRIPTION</span></span>
<span data-ttu-id="5173f-109">Remove-AzSqlElasticJobCredential cmdlet은 작업 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5173f-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="5173f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5173f-110">EXAMPLES</span></span>

### <span data-ttu-id="5173f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5173f-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="5173f-112">작업 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="5173f-112">Removes a job credential</span></span>

## <span data-ttu-id="5173f-113">변수</span><span class="sxs-lookup"><span data-stu-id="5173f-113">PARAMETERS</span></span>

### <span data-ttu-id="5173f-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5173f-114">-AgentName</span></span>
<span data-ttu-id="5173f-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="5173f-115">The agent name</span></span>

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

### <span data-ttu-id="5173f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5173f-116">-DefaultProfile</span></span>
<span data-ttu-id="5173f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5173f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5173f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5173f-118">-InputObject</span></span>
<span data-ttu-id="5173f-119">작업 자격 증명 개체</span><span class="sxs-lookup"><span data-stu-id="5173f-119">The job credential object</span></span>

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

### <span data-ttu-id="5173f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="5173f-120">-Name</span></span>
<span data-ttu-id="5173f-121">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="5173f-121">The job credential name</span></span>

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

### <span data-ttu-id="5173f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5173f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5173f-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5173f-123">The resource group name</span></span>

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

### <span data-ttu-id="5173f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5173f-124">-ResourceId</span></span>
<span data-ttu-id="5173f-125">작업 자격 증명 리소스 id</span><span class="sxs-lookup"><span data-stu-id="5173f-125">The job credential resource id</span></span>

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

### <span data-ttu-id="5173f-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5173f-126">-ServerName</span></span>
<span data-ttu-id="5173f-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="5173f-127">The server name</span></span>

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

### <span data-ttu-id="5173f-128">-확인</span><span class="sxs-lookup"><span data-stu-id="5173f-128">-Confirm</span></span>
<span data-ttu-id="5173f-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5173f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5173f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5173f-130">-WhatIf</span></span>
<span data-ttu-id="5173f-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5173f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5173f-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5173f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5173f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5173f-133">CommonParameters</span></span>
<span data-ttu-id="5173f-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5173f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5173f-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5173f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5173f-136">입력</span><span class="sxs-lookup"><span data-stu-id="5173f-136">INPUTS</span></span>

### <span data-ttu-id="5173f-137">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="5173f-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="5173f-138">출력</span><span class="sxs-lookup"><span data-stu-id="5173f-138">OUTPUTS</span></span>

### <span data-ttu-id="5173f-139">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="5173f-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="5173f-140">상속자</span><span class="sxs-lookup"><span data-stu-id="5173f-140">NOTES</span></span>

## <span data-ttu-id="5173f-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5173f-141">RELATED LINKS</span></span>
