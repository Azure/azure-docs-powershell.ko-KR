---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7f2589c665bd24fdb2d017cd8cfd4ca055e3e429
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999456"
---
# <span data-ttu-id="5b8af-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="5b8af-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="5b8af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b8af-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8af-103">로그 재생 서비스 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="5b8af-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b8af-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b8af-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b8af-105">DESCRIPTION</span></span>
<span data-ttu-id="5b8af-106">**Get-AzSqlInstanceDatabaseLogReplay** cmdlet은 주어진 데이터베이스에서 Log Replay 서비스 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="5b8af-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b8af-107">EXAMPLES</span></span>

### <span data-ttu-id="5b8af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b8af-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="5b8af-109">이 명령은 주어진 데이터베이스에 로그 재생 서비스 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="5b8af-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b8af-110">PARAMETERS</span></span>

### <span data-ttu-id="5b8af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8af-111">-DefaultProfile</span></span>
<span data-ttu-id="5b8af-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b8af-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5b8af-113">-InstanceName</span></span>
<span data-ttu-id="5b8af-114">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8af-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5b8af-115">-Name</span></span>
<span data-ttu-id="5b8af-116">검색할 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b8af-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b8af-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8af-119">CommonParameters</span></span>
<span data-ttu-id="5b8af-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8af-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b8af-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8af-122">입력</span><span class="sxs-lookup"><span data-stu-id="5b8af-122">INPUTS</span></span>

### <span data-ttu-id="5b8af-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5b8af-123">System.String</span></span>

## <span data-ttu-id="5b8af-124">출력</span><span class="sxs-lookup"><span data-stu-id="5b8af-124">OUTPUTS</span></span>

### <span data-ttu-id="5b8af-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="5b8af-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="5b8af-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b8af-126">NOTES</span></span>

## <span data-ttu-id="5b8af-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b8af-127">RELATED LINKS</span></span>
