---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 186ff32138bba0556b05e9674f1711e9425a20c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873729"
---
# <span data-ttu-id="eb5e3-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="eb5e3-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="eb5e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5e3-103">데이터베이스에 대 한 고급 위협 보호 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="eb5e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb5e3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb5e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eb5e3-105">DESCRIPTION</span></span>
<span data-ttu-id="eb5e3-106">**AzSqlDatabaseAdvancedThreatProtectionSettings** Cmdlet은 Azure SQL 데이터베이스의 고급 위협 방지 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="eb5e3-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여이 cmdlet에 설정 된 설정을 가져오는 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="eb5e3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="eb5e3-108">EXAMPLES</span></span>

### <span data-ttu-id="eb5e3-109">예제 1: 데이터베이스에 대 한 고급 위협 보호 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="eb5e3-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="eb5e3-110">이 명령은 Database01 이라는 데이터베이스에 대 한 고급 위협 보호 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="eb5e3-111">데이터베이스는 리소스 그룹 ResourceGroup11에 할당 되는 Server01 이라는 서버에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="eb5e3-112">변수</span><span class="sxs-lookup"><span data-stu-id="eb5e3-112">PARAMETERS</span></span>

### <span data-ttu-id="eb5e3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb5e3-113">-DatabaseName</span></span>
<span data-ttu-id="eb5e3-114">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="eb5e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5e3-115">-DefaultProfile</span></span>
<span data-ttu-id="eb5e3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eb5e3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb5e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb5e3-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eb5e3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb5e3-119">-ServerName</span></span>
<span data-ttu-id="eb5e3-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="eb5e3-121">-확인</span><span class="sxs-lookup"><span data-stu-id="eb5e3-121">-Confirm</span></span>
<span data-ttu-id="eb5e3-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb5e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5e3-123">-WhatIf</span></span>
<span data-ttu-id="eb5e3-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb5e3-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb5e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5e3-126">CommonParameters</span></span>
<span data-ttu-id="eb5e3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb5e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5e3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb5e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5e3-129">입력</span><span class="sxs-lookup"><span data-stu-id="eb5e3-129">INPUTS</span></span>

### <span data-ttu-id="eb5e3-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb5e3-130">System.String</span></span>

## <span data-ttu-id="eb5e3-131">출력</span><span class="sxs-lookup"><span data-stu-id="eb5e3-131">OUTPUTS</span></span>

### <span data-ttu-id="eb5e3-132">ThreatDetection. DatabaseAdvancedThreatProtectionSettingsModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="eb5e3-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="eb5e3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="eb5e3-133">NOTES</span></span>

## <span data-ttu-id="eb5e3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb5e3-134">RELATED LINKS</span></span>

[<span data-ttu-id="eb5e3-135">제거-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="eb5e3-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)



