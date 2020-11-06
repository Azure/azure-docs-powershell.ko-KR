---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1b8e99b195866ac63f649d4484a0cfb631b09e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524800"
---
# <span data-ttu-id="68122-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="68122-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="68122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68122-102">SYNOPSIS</span></span>
<span data-ttu-id="68122-103">SQL 데이터베이스 서버의 업그레이드를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68122-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68122-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68122-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68122-105">DESCRIPTION</span></span>
<span data-ttu-id="68122-106">**AzureRmSqlServerUpgrade** Cmdlet은 Azure SQL 데이터베이스 서버의 업그레이드를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="68122-107">예제의</span><span class="sxs-lookup"><span data-stu-id="68122-107">EXAMPLES</span></span>

### <span data-ttu-id="68122-108">예제 1: 서버 업그레이드 중지</span><span class="sxs-lookup"><span data-stu-id="68122-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="68122-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에 할당 된 Server02 서버를 업그레이드 하는 요청을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="68122-110">변수</span><span class="sxs-lookup"><span data-stu-id="68122-110">PARAMETERS</span></span>

### <span data-ttu-id="68122-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68122-111">-DefaultProfile</span></span>
<span data-ttu-id="68122-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="68122-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68122-113">-Force</span><span class="sxs-lookup"><span data-stu-id="68122-113">-Force</span></span>
<span data-ttu-id="68122-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68122-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68122-115">-ResourceGroupName</span></span>
<span data-ttu-id="68122-116">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="68122-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68122-117">-ServerName</span></span>
<span data-ttu-id="68122-118">이 cmdlet이 업그레이드를 중지 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68122-119">-확인</span><span class="sxs-lookup"><span data-stu-id="68122-119">-Confirm</span></span>
<span data-ttu-id="68122-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68122-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68122-121">-WhatIf</span></span>
<span data-ttu-id="68122-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68122-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68122-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68122-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68122-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68122-124">CommonParameters</span></span>
<span data-ttu-id="68122-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68122-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68122-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68122-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68122-127">입력</span><span class="sxs-lookup"><span data-stu-id="68122-127">INPUTS</span></span>

### <span data-ttu-id="68122-128">AzureSqlServerUpgradeModel 업그레이드. 모델. m a.</span><span class="sxs-lookup"><span data-stu-id="68122-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="68122-129">출력</span><span class="sxs-lookup"><span data-stu-id="68122-129">OUTPUTS</span></span>

## <span data-ttu-id="68122-130">상속자</span><span class="sxs-lookup"><span data-stu-id="68122-130">NOTES</span></span>

## <span data-ttu-id="68122-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68122-131">RELATED LINKS</span></span>

[<span data-ttu-id="68122-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="68122-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="68122-133">시작-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="68122-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="68122-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="68122-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


