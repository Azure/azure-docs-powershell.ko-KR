---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 6cb14b368bf7f190c30ff32fdec12576d3189204
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699011"
---
# <span data-ttu-id="e4420-101">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4420-101">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="e4420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4420-102">SYNOPSIS</span></span>
<span data-ttu-id="e4420-103">데이터베이스에 대 한 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-103">Gets the threat detection policy for a database.</span></span>

## <span data-ttu-id="e4420-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4420-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4420-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e4420-105">DESCRIPTION</span></span>
<span data-ttu-id="e4420-106">**AzSqlDatabaseThreatDetectionPolicy** Cmdlet은 Azure SQL 데이터베이스의 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-106">The **Get-AzSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="e4420-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여이 cmdlet이 정책을 가져오는 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="e4420-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e4420-108">EXAMPLES</span></span>

### <span data-ttu-id="e4420-109">예제 1: 데이터베이스에 대 한 위협 검색 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="e4420-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="e4420-110">이 명령은 Database01 이라는 데이터베이스에 대 한 위협 검색 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="e4420-111">데이터베이스는 리소스 그룹 ResourceGroup11에 할당 되는 Server01 이라는 서버에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="e4420-112">변수</span><span class="sxs-lookup"><span data-stu-id="e4420-112">PARAMETERS</span></span>

### <span data-ttu-id="e4420-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4420-113">-DatabaseName</span></span>
<span data-ttu-id="e4420-114">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="e4420-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4420-115">-DefaultProfile</span></span>
<span data-ttu-id="e4420-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e4420-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4420-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4420-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4420-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e4420-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e4420-119">-ServerName</span></span>
<span data-ttu-id="e4420-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="e4420-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e4420-121">-Confirm</span></span>
<span data-ttu-id="e4420-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4420-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4420-123">-WhatIf</span></span>
<span data-ttu-id="e4420-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4420-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4420-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4420-126">CommonParameters</span></span>
<span data-ttu-id="e4420-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4420-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4420-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4420-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4420-129">입력</span><span class="sxs-lookup"><span data-stu-id="e4420-129">INPUTS</span></span>

### <span data-ttu-id="e4420-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4420-130">System.String</span></span>

## <span data-ttu-id="e4420-131">출력</span><span class="sxs-lookup"><span data-stu-id="e4420-131">OUTPUTS</span></span>

### <span data-ttu-id="e4420-132">ThreatDetection. DatabaseThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e4420-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="e4420-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e4420-133">NOTES</span></span>

## <span data-ttu-id="e4420-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4420-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4420-135">제거-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4420-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)



