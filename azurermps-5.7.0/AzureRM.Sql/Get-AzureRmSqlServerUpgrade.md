---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c1be584b1110f720d1d5d50b32d7efa5d8586db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703951"
---
# <span data-ttu-id="62477-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="62477-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="62477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62477-102">SYNOPSIS</span></span>
<span data-ttu-id="62477-103">Azure SQL 데이터베이스 서버 업그레이드의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62477-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62477-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62477-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62477-105">설명은</span><span class="sxs-lookup"><span data-stu-id="62477-105">DESCRIPTION</span></span>
<span data-ttu-id="62477-106">**AzureRmSqlServerUpgrade** Cmdlet은 Azure SQL 데이터베이스 서버 업그레이드의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62477-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="62477-107">예제의</span><span class="sxs-lookup"><span data-stu-id="62477-107">EXAMPLES</span></span>

### <span data-ttu-id="62477-108">예제 1: 업그레이드 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="62477-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="62477-109">이 명령은 ResourceGroup01 이라는 리소스 그룹의 Server01 이라는 서버에서 업그레이드의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62477-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="62477-110">변수</span><span class="sxs-lookup"><span data-stu-id="62477-110">PARAMETERS</span></span>

### <span data-ttu-id="62477-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62477-111">-DefaultProfile</span></span>
<span data-ttu-id="62477-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="62477-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62477-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62477-113">-ResourceGroupName</span></span>
<span data-ttu-id="62477-114">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62477-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="62477-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62477-115">-ServerName</span></span>
<span data-ttu-id="62477-116">이 cmdlet이 업그레이드 상태를 가져오는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62477-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="62477-117">-확인</span><span class="sxs-lookup"><span data-stu-id="62477-117">-Confirm</span></span>
<span data-ttu-id="62477-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="62477-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62477-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62477-119">-WhatIf</span></span>
<span data-ttu-id="62477-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62477-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62477-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62477-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62477-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62477-122">CommonParameters</span></span>
<span data-ttu-id="62477-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62477-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62477-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62477-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62477-125">입력</span><span class="sxs-lookup"><span data-stu-id="62477-125">INPUTS</span></span>

### <span data-ttu-id="62477-126">않아야</span><span class="sxs-lookup"><span data-stu-id="62477-126">None</span></span>
<span data-ttu-id="62477-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62477-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62477-128">출력</span><span class="sxs-lookup"><span data-stu-id="62477-128">OUTPUTS</span></span>

### <span data-ttu-id="62477-129">AzureSqlServerUpgradeModel 업그레이드. 모델. m a.</span><span class="sxs-lookup"><span data-stu-id="62477-129">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="62477-130">상속자</span><span class="sxs-lookup"><span data-stu-id="62477-130">NOTES</span></span>

## <span data-ttu-id="62477-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62477-131">RELATED LINKS</span></span>

[<span data-ttu-id="62477-132">시작-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="62477-132">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="62477-133">중지-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="62477-133">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="62477-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="62477-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


