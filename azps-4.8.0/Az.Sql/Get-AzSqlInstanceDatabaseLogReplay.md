---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213249"
---
# <span data-ttu-id="3fad3-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="3fad3-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="3fad3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fad3-102">SYNOPSIS</span></span>
<span data-ttu-id="3fad3-103">로그 재생 서비스 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="3fad3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fad3-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fad3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3fad3-105">DESCRIPTION</span></span>
<span data-ttu-id="3fad3-106">**AzSqlInstanceDatabaseLogReplay** cmdlet은 지정 된 데이터베이스의 로그 재생 서비스 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="3fad3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3fad3-107">EXAMPLES</span></span>

### <span data-ttu-id="3fad3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fad3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="3fad3-109">이 명령은 지정 된 데이터베이스에서 로그 재생 서비스 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="3fad3-110">변수</span><span class="sxs-lookup"><span data-stu-id="3fad3-110">PARAMETERS</span></span>

### <span data-ttu-id="3fad3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fad3-111">-DefaultProfile</span></span>
<span data-ttu-id="3fad3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fad3-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3fad3-113">-InstanceName</span></span>
<span data-ttu-id="3fad3-114">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-114">The name of the instance.</span></span>

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

### <span data-ttu-id="3fad3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3fad3-115">-Name</span></span>
<span data-ttu-id="3fad3-116">검색할 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="3fad3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fad3-117">-ResourceGroupName</span></span>
<span data-ttu-id="3fad3-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3fad3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fad3-119">CommonParameters</span></span>
<span data-ttu-id="3fad3-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fad3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fad3-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3fad3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fad3-122">입력</span><span class="sxs-lookup"><span data-stu-id="3fad3-122">INPUTS</span></span>

### <span data-ttu-id="3fad3-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3fad3-123">System.String</span></span>

## <span data-ttu-id="3fad3-124">출력</span><span class="sxs-lookup"><span data-stu-id="3fad3-124">OUTPUTS</span></span>

### <span data-ttu-id="3fad3-125">AzureSqlManagedDatabaseRestoreDetailsResultModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="3fad3-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="3fad3-126">상속자</span><span class="sxs-lookup"><span data-stu-id="3fad3-126">NOTES</span></span>

## <span data-ttu-id="3fad3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fad3-127">RELATED LINKS</span></span>
