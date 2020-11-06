---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 588954527c76bb0f5394afe4df9e19b37c10fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526556"
---
# <span data-ttu-id="2f7e9-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f7e9-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2f7e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7e9-103">데이터베이스 서버 복구 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f7e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f7e9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f7e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2f7e9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f7e9-106">**AzureRmSqlServerDisasterRecoveryConfiguration** CMDLET은 SQL 데이터베이스 서버 복구 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="2f7e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2f7e9-107">EXAMPLES</span></span>

## <span data-ttu-id="2f7e9-108">변수</span><span class="sxs-lookup"><span data-stu-id="2f7e9-108">PARAMETERS</span></span>

### <span data-ttu-id="2f7e9-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="2f7e9-109">-AllowDataLoss</span></span>
<span data-ttu-id="2f7e9-110">장애 조치 (failover) 작업을 통해 데이터 손실이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="2f7e9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f7e9-111">-AsJob</span></span>
<span data-ttu-id="2f7e9-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2f7e9-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7e9-113">-DefaultProfile</span></span>
<span data-ttu-id="2f7e9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2f7e9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f7e9-115">-장애 조치</span><span class="sxs-lookup"><span data-stu-id="2f7e9-115">-Failover</span></span>
<span data-ttu-id="2f7e9-116">이 작업이 장애 조치 (failover) 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f7e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f7e9-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2f7e9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f7e9-119">-ServerName</span></span>
<span data-ttu-id="2f7e9-120">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="2f7e9-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2f7e9-121">-VirtualEndpointName</span></span>
<span data-ttu-id="2f7e9-122">가상 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7e9-123">-확인</span><span class="sxs-lookup"><span data-stu-id="2f7e9-123">-Confirm</span></span>
<span data-ttu-id="2f7e9-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7e9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f7e9-125">-WhatIf</span></span>
<span data-ttu-id="2f7e9-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f7e9-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7e9-128">CommonParameters</span></span>
<span data-ttu-id="2f7e9-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7e9-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f7e9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7e9-131">입력</span><span class="sxs-lookup"><span data-stu-id="2f7e9-131">INPUTS</span></span>

### <span data-ttu-id="2f7e9-132">않아야</span><span class="sxs-lookup"><span data-stu-id="2f7e9-132">None</span></span>
<span data-ttu-id="2f7e9-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f7e9-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f7e9-134">출력</span><span class="sxs-lookup"><span data-stu-id="2f7e9-134">OUTPUTS</span></span>

## <span data-ttu-id="2f7e9-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2f7e9-135">NOTES</span></span>

## <span data-ttu-id="2f7e9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f7e9-136">RELATED LINKS</span></span>

[<span data-ttu-id="2f7e9-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f7e9-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f7e9-138">새로운 AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f7e9-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f7e9-139">제거-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f7e9-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f7e9-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2f7e9-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
