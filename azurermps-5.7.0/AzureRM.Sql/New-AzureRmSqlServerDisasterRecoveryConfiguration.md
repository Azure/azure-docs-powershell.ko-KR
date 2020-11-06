---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531606"
---
# <span data-ttu-id="b269a-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b269a-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="b269a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b269a-102">SYNOPSIS</span></span>
<span data-ttu-id="b269a-103">데이터베이스 서버 시스템 복구 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b269a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b269a-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b269a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b269a-105">DESCRIPTION</span></span>
<span data-ttu-id="b269a-106">**AzureRmSqlServerDisasterRecoveryConfiguration** CMDLET은 SQL 데이터베이스 서버 시스템 복구 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="b269a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b269a-107">EXAMPLES</span></span>

## <span data-ttu-id="b269a-108">변수</span><span class="sxs-lookup"><span data-stu-id="b269a-108">PARAMETERS</span></span>

### <span data-ttu-id="b269a-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b269a-109">-AsJob</span></span>
<span data-ttu-id="b269a-110">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b269a-110">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="b269a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b269a-111">-DefaultProfile</span></span>
<span data-ttu-id="b269a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b269a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b269a-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="b269a-113">-FailoverPolicy</span></span>
<span data-ttu-id="b269a-114">장애 조치 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-114">Specifies the failover policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b269a-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b269a-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b269a-116">파트너 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="b269a-117">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="b269a-117">-PartnerServerName</span></span>
<span data-ttu-id="b269a-118">파트너 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="b269a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b269a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b269a-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b269a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b269a-121">-ServerName</span></span>
<span data-ttu-id="b269a-122">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b269a-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="b269a-123">-VirtualEndpointName</span></span>
<span data-ttu-id="b269a-124">가상 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="b269a-125">-확인</span><span class="sxs-lookup"><span data-stu-id="b269a-125">-Confirm</span></span>
<span data-ttu-id="b269a-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b269a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b269a-127">-WhatIf</span></span>
<span data-ttu-id="b269a-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b269a-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b269a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b269a-130">CommonParameters</span></span>
<span data-ttu-id="b269a-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b269a-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b269a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b269a-133">입력</span><span class="sxs-lookup"><span data-stu-id="b269a-133">INPUTS</span></span>

### <span data-ttu-id="b269a-134">않아야</span><span class="sxs-lookup"><span data-stu-id="b269a-134">None</span></span>
<span data-ttu-id="b269a-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b269a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b269a-136">출력</span><span class="sxs-lookup"><span data-stu-id="b269a-136">OUTPUTS</span></span>

## <span data-ttu-id="b269a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b269a-137">NOTES</span></span>

## <span data-ttu-id="b269a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b269a-138">RELATED LINKS</span></span>

[<span data-ttu-id="b269a-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b269a-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b269a-140">제거-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b269a-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b269a-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b269a-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b269a-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b269a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
