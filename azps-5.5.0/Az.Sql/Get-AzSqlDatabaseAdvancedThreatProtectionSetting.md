---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9035f2a03ac04a9bc99248c48675ab3c69b84207
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409616"
---
# <span data-ttu-id="28be4-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="28be4-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="28be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28be4-102">SYNOPSIS</span></span>
<span data-ttu-id="28be4-103">데이터베이스에 대한 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="28be4-104">구문</span><span class="sxs-lookup"><span data-stu-id="28be4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28be4-105">설명</span><span class="sxs-lookup"><span data-stu-id="28be4-105">DESCRIPTION</span></span>
<span data-ttu-id="28be4-106">**Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet은 Azure SQL 데이터베이스의 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="28be4-107">이 cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 지정하여 이 cmdlet에서 설정을 얻을 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="28be4-108">예제</span><span class="sxs-lookup"><span data-stu-id="28be4-108">EXAMPLES</span></span>

### <span data-ttu-id="28be4-109">예제 1: 데이터베이스에 대한 고급 위협 방지 설정 사용</span><span class="sxs-lookup"><span data-stu-id="28be4-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="28be4-110">이 명령은 Database01이라는 데이터베이스에 대한 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="28be4-111">데이터베이스는 리소스 그룹 ResourceGroup11에 할당된 Server01이라는 서버에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="28be4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28be4-112">PARAMETERS</span></span>

### <span data-ttu-id="28be4-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28be4-113">-DatabaseName</span></span>
<span data-ttu-id="28be4-114">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="28be4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28be4-115">-DefaultProfile</span></span>
<span data-ttu-id="28be4-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="28be4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28be4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28be4-117">-ResourceGroupName</span></span>
<span data-ttu-id="28be4-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="28be4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28be4-119">-ServerName</span></span>
<span data-ttu-id="28be4-120">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="28be4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28be4-121">-Confirm</span></span>
<span data-ttu-id="28be4-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28be4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28be4-123">-WhatIf</span></span>
<span data-ttu-id="28be4-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="28be4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28be4-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28be4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28be4-126">CommonParameters</span></span>
<span data-ttu-id="28be4-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28be4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28be4-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28be4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28be4-129">입력</span><span class="sxs-lookup"><span data-stu-id="28be4-129">INPUTS</span></span>

### <span data-ttu-id="28be4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="28be4-130">System.String</span></span>

## <span data-ttu-id="28be4-131">출력</span><span class="sxs-lookup"><span data-stu-id="28be4-131">OUTPUTS</span></span>

### <span data-ttu-id="28be4-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="28be4-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="28be4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28be4-133">NOTES</span></span>

## <span data-ttu-id="28be4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28be4-134">RELATED LINKS</span></span>




