---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204818"
---
# <span data-ttu-id="9c25e-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9c25e-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9c25e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c25e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c25e-103">서버에 대 한 고급 위협 방지 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="9c25e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c25e-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c25e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9c25e-105">DESCRIPTION</span></span>
<span data-ttu-id="9c25e-106">**AzSqlServerAdvancedThreatProtectionSetting** Cmdlet은 Azure SQL server의 고급 위협 방지 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="9c25e-107">이 cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 하 여이 cmdlet에 설정 된 설정을 가져오는 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="9c25e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9c25e-108">EXAMPLES</span></span>

### <span data-ttu-id="9c25e-109">예제 1: 서버에 대 한 고급 위협 방지 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="9c25e-109">Example 1: Get the advanced threat protection settings for a server</span></span>
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

<span data-ttu-id="9c25e-110">이 명령은 Server01 이라는 서버에 대 한 고급 위협 보호 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="9c25e-111">서버가 리소스 그룹 ResourceGroup11에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="9c25e-112">변수</span><span class="sxs-lookup"><span data-stu-id="9c25e-112">PARAMETERS</span></span>

### <span data-ttu-id="9c25e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c25e-113">-DefaultProfile</span></span>
<span data-ttu-id="9c25e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9c25e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c25e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c25e-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c25e-116">서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="9c25e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c25e-117">-ServerName</span></span>
<span data-ttu-id="9c25e-118">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9c25e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="9c25e-119">-Confirm</span></span>
<span data-ttu-id="9c25e-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c25e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c25e-121">-WhatIf</span></span>
<span data-ttu-id="9c25e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c25e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c25e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c25e-124">CommonParameters</span></span>
<span data-ttu-id="9c25e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c25e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c25e-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c25e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c25e-127">입력</span><span class="sxs-lookup"><span data-stu-id="9c25e-127">INPUTS</span></span>

### <span data-ttu-id="9c25e-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c25e-128">System.String</span></span>

## <span data-ttu-id="9c25e-129">출력</span><span class="sxs-lookup"><span data-stu-id="9c25e-129">OUTPUTS</span></span>

### <span data-ttu-id="9c25e-130">ThreatDetection. ServerAdvancedThreatProtectionSettingsModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9c25e-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="9c25e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9c25e-131">NOTES</span></span>

## <span data-ttu-id="9c25e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c25e-132">RELATED LINKS</span></span>

[<span data-ttu-id="9c25e-133">제거-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9c25e-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="9c25e-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9c25e-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


