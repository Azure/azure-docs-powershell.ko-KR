---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376531"
---
# <span data-ttu-id="b1d10-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b1d10-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="b1d10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1d10-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d10-103">서버에 대한 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="b1d10-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1d10-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1d10-105">설명</span><span class="sxs-lookup"><span data-stu-id="b1d10-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d10-106">**Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet은 Azure SQL 서버의 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="b1d10-107">이 cmdlet을 사용하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정하여 이 cmdlet이 설정을 받을 서버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="b1d10-108">예제</span><span class="sxs-lookup"><span data-stu-id="b1d10-108">EXAMPLES</span></span>

### <span data-ttu-id="b1d10-109">예제 1: 서버에 대한 고급 위협 방지 설정 얻기</span><span class="sxs-lookup"><span data-stu-id="b1d10-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="b1d10-110">이 명령은 Server01이라는 서버에 대한 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="b1d10-111">서버가 리소스 그룹 ResourceGroup11에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="b1d10-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1d10-112">PARAMETERS</span></span>

### <span data-ttu-id="b1d10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d10-113">-DefaultProfile</span></span>
<span data-ttu-id="b1d10-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b1d10-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1d10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d10-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1d10-116">서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="b1d10-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1d10-117">-ServerName</span></span>
<span data-ttu-id="b1d10-118">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-118">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d10-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1d10-119">-Confirm</span></span>
<span data-ttu-id="b1d10-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1d10-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1d10-121">-WhatIf</span></span>
<span data-ttu-id="b1d10-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1d10-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1d10-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1d10-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d10-124">CommonParameters</span></span>
<span data-ttu-id="b1d10-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d10-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d10-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1d10-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d10-127">입력</span><span class="sxs-lookup"><span data-stu-id="b1d10-127">INPUTS</span></span>

### <span data-ttu-id="b1d10-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1d10-128">System.String</span></span>

## <span data-ttu-id="b1d10-129">출력</span><span class="sxs-lookup"><span data-stu-id="b1d10-129">OUTPUTS</span></span>

### <span data-ttu-id="b1d10-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="b1d10-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="b1d10-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1d10-131">NOTES</span></span>

## <span data-ttu-id="b1d10-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1d10-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1d10-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b1d10-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="b1d10-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b1d10-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


