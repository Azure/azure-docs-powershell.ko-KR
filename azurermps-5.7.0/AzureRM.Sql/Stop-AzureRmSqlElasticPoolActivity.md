---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 87744454627feaadc8c953e1ad4e50016f14879f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532595"
---
# <span data-ttu-id="b0511-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b0511-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="b0511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0511-102">SYNOPSIS</span></span>
<span data-ttu-id="b0511-103">탄력적 풀에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0511-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0511-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0511-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0511-105">DESCRIPTION</span></span>
<span data-ttu-id="b0511-106">**AzureRmSqlElasticPoolActivity** cmdlet은 탄력적 풀에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="b0511-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0511-107">EXAMPLES</span></span>

### <span data-ttu-id="b0511-108">예제 1: 탄력적 풀에서 비동기 업데이트 작업 취소</span><span class="sxs-lookup"><span data-stu-id="b0511-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
```

<span data-ttu-id="b0511-109">이 명령은 탄력적 풀에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="b0511-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0511-110">PARAMETERS</span></span>

### <span data-ttu-id="b0511-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0511-111">-DefaultProfile</span></span>
<span data-ttu-id="b0511-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0511-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b0511-113">-ElasticPoolName</span></span>
<span data-ttu-id="b0511-114">Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0511-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b0511-115">-OperationId</span></span>
<span data-ttu-id="b0511-116">검색할 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0511-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0511-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0511-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0511-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0511-119">-ServerName</span></span>
<span data-ttu-id="b0511-120">탄력적인 풀이 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-120">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0511-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b0511-121">-Confirm</span></span>
<span data-ttu-id="b0511-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0511-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0511-123">-WhatIf</span></span>
<span data-ttu-id="b0511-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0511-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0511-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0511-126">CommonParameters</span></span>
<span data-ttu-id="b0511-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0511-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0511-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0511-129">입력</span><span class="sxs-lookup"><span data-stu-id="b0511-129">INPUTS</span></span>

### <span data-ttu-id="b0511-130">않아야</span><span class="sxs-lookup"><span data-stu-id="b0511-130">None</span></span>

<span data-ttu-id="b0511-131">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0511-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b0511-132">출력</span><span class="sxs-lookup"><span data-stu-id="b0511-132">OUTPUTS</span></span>

### <span data-ttu-id="b0511-133">System. 개체</span><span class="sxs-lookup"><span data-stu-id="b0511-133">System.Object</span></span>

## <span data-ttu-id="b0511-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b0511-134">NOTES</span></span>

## <span data-ttu-id="b0511-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0511-135">RELATED LINKS</span></span>



