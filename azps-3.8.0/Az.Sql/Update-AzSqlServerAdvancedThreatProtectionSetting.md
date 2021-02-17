---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 079a1254865821b77ca48a94256dbe1a9e4cb431
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415328"
---
# <span data-ttu-id="ba6d4-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="ba6d4-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="ba6d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6d4-103">서버에서 고급 위협 보호 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="ba6d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba6d4-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba6d4-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba6d4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba6d4-106">**Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet은 Azure SQL 서버에서 고급 위협 보호 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="ba6d4-107">서버에서 고급 위협 방지를 사용하도록 설정하려면 해당 서버에서 감사 설정을 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="ba6d4-108">이 cmdlet을 사용 하 고 서버를 식별 하는 *ResourceGroupName* 및 ServerName 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="ba6d4-109">예제</span><span class="sxs-lookup"><span data-stu-id="ba6d4-109">EXAMPLES</span></span>

### <span data-ttu-id="ba6d4-110">예제 1: 데이터베이스에 대한 고급 위협 방지 설정 설정</span><span class="sxs-lookup"><span data-stu-id="ba6d4-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="ba6d4-111">이 명령은 Server01이라는 서버에 대한 고급 위협 보호 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="ba6d4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba6d4-112">PARAMETERS</span></span>

### <span data-ttu-id="ba6d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6d4-113">-DefaultProfile</span></span>
<span data-ttu-id="ba6d4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ba6d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba6d4-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ba6d4-115">-EmailAdmins</span></span>
<span data-ttu-id="ba6d4-116">고급 위협 방지 설정이 전자 메일을 사용하여 관리자에게 연락하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6d4-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="ba6d4-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="ba6d4-118">설정에서 제외할 검색 유형의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="ba6d4-119">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="ba6d4-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba6d4-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="ba6d4-120">Sql_Injection</span></span>
- <span data-ttu-id="ba6d4-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="ba6d4-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="ba6d4-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="ba6d4-122">Access_Anomaly</span></span>
- <span data-ttu-id="ba6d4-123">없음</span><span class="sxs-lookup"><span data-stu-id="ba6d4-123">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6d4-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="ba6d4-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="ba6d4-125">설정에서 경고를 보내는 세미코론으로 구분된 전자 메일 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6d4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba6d4-126">-PassThru</span></span>
<span data-ttu-id="ba6d4-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba6d4-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba6d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba6d4-130">서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="ba6d4-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ba6d4-131">-RetentionInDays</span></span>
<span data-ttu-id="ba6d4-132">감사 로그의 보존 기간(일)</span><span class="sxs-lookup"><span data-stu-id="ba6d4-132">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6d4-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba6d4-133">-ServerName</span></span>
<span data-ttu-id="ba6d4-134">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ba6d4-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba6d4-135">-StorageAccountName</span></span>
<span data-ttu-id="ba6d4-136">사용할 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="ba6d4-137">와일드카드는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-137">Wildcards are not permitted.</span></span> <span data-ttu-id="ba6d4-138">이 매개 변수는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-138">This parameter is not required.</span></span> <span data-ttu-id="ba6d4-139">이 매개 변수가 제공되지 않은 경우 cmdlet은 데이터베이스의 고급 위협 보호 설정의 일부로 이전에 정의된 저장소 계정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="ba6d4-140">데이터베이스 위협 감지 설정이 처음으로 정의되고 이 매개 변수가 제공되지 않은 경우 cmdlet이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6d4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba6d4-141">-Confirm</span></span>
<span data-ttu-id="ba6d4-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba6d4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6d4-143">-WhatIf</span></span>
<span data-ttu-id="ba6d4-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ba6d4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba6d4-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba6d4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6d4-146">CommonParameters</span></span>
<span data-ttu-id="ba6d4-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6d4-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba6d4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6d4-149">입력</span><span class="sxs-lookup"><span data-stu-id="ba6d4-149">INPUTS</span></span>

### <span data-ttu-id="ba6d4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ba6d4-150">System.String</span></span>

### <span data-ttu-id="ba6d4-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ba6d4-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ba6d4-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="ba6d4-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="ba6d4-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ba6d4-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ba6d4-154">출력</span><span class="sxs-lookup"><span data-stu-id="ba6d4-154">OUTPUTS</span></span>

### <span data-ttu-id="ba6d4-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="ba6d4-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="ba6d4-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba6d4-156">NOTES</span></span>

## <span data-ttu-id="ba6d4-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba6d4-157">RELATED LINKS</span></span>

[<span data-ttu-id="ba6d4-158">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ba6d4-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
