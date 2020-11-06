---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 9b51a9e835962ea1715a458ace1ab02202068e30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531901"
---
# <span data-ttu-id="36324-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="36324-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="36324-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36324-102">SYNOPSIS</span></span>
<span data-ttu-id="36324-103">데이터베이스에서 위협 검색 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36324-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36324-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36324-105">설명은</span><span class="sxs-lookup"><span data-stu-id="36324-105">DESCRIPTION</span></span>
<span data-ttu-id="36324-106">**AzureRmSqlDatabaseThreatDetectionPolicy** Cmdlet은 AZUREAZURE SQL 데이터베이스에서 위협 검색 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="36324-107">이 cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 하 여이 cmdlet이 정책을 제거 하는 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="36324-108">예제의</span><span class="sxs-lookup"><span data-stu-id="36324-108">EXAMPLES</span></span>

### <span data-ttu-id="36324-109">예제 1: 데이터베이스에 대 한 위협 검색 정책 제거</span><span class="sxs-lookup"><span data-stu-id="36324-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="36324-110">이 명령은 Server01 이라는 서버의 Database01 이라는 데이터베이스에서 위협 검색 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="36324-111">변수</span><span class="sxs-lookup"><span data-stu-id="36324-111">PARAMETERS</span></span>

### <span data-ttu-id="36324-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36324-112">-DatabaseName</span></span>
<span data-ttu-id="36324-113">위협 검색 정책을 제거할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="36324-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36324-114">-DefaultProfile</span></span>
<span data-ttu-id="36324-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="36324-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36324-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36324-116">-PassThru</span></span>
<span data-ttu-id="36324-117">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36324-118">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36324-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36324-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36324-119">-ResourceGroupName</span></span>
<span data-ttu-id="36324-120">서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-120">Specifies the name of the resource group the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36324-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36324-121">-ServerName</span></span>
<span data-ttu-id="36324-122">데이터베이스가 실행 되는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-122">Specifies the name of a server on which the database runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36324-123">-확인</span><span class="sxs-lookup"><span data-stu-id="36324-123">-Confirm</span></span>
<span data-ttu-id="36324-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36324-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36324-125">-WhatIf</span></span>
<span data-ttu-id="36324-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="36324-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36324-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36324-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36324-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36324-128">CommonParameters</span></span>
<span data-ttu-id="36324-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36324-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36324-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36324-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36324-131">입력</span><span class="sxs-lookup"><span data-stu-id="36324-131">INPUTS</span></span>

### <span data-ttu-id="36324-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="36324-132">System.String</span></span>

## <span data-ttu-id="36324-133">출력</span><span class="sxs-lookup"><span data-stu-id="36324-133">OUTPUTS</span></span>

### <span data-ttu-id="36324-134">ThreatDetection. DatabaseThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="36324-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="36324-135">상속자</span><span class="sxs-lookup"><span data-stu-id="36324-135">NOTES</span></span>

## <span data-ttu-id="36324-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36324-136">RELATED LINKS</span></span>

[<span data-ttu-id="36324-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="36324-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


