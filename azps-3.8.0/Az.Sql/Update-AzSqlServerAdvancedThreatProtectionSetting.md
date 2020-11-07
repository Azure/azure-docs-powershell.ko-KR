---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878677"
---
# <span data-ttu-id="52979-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="52979-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="52979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52979-102">SYNOPSIS</span></span>
<span data-ttu-id="52979-103">서버에서 고급 위협 방지 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="52979-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52979-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52979-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52979-105">DESCRIPTION</span></span>
<span data-ttu-id="52979-106">**AzSqlServerAdvancedThreatProtectionSetting** Cmdlet은 Azure SQL server에서 고급 위협 방지 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="52979-107">서버에서 고급 위협 보호를 사용 하도록 설정 하려면 해당 서버에서 감사 설정을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="52979-108">이 cmdlet을 사용 하려면 서버를 식별 하는 *ResourceGroupName* 및 ServerName 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="52979-109">예제의</span><span class="sxs-lookup"><span data-stu-id="52979-109">EXAMPLES</span></span>

### <span data-ttu-id="52979-110">예제 1: 데이터베이스에 대 한 고급 위협 보호 설정 설정</span><span class="sxs-lookup"><span data-stu-id="52979-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="52979-111">이 명령은 Server01 라는 서버에 대 한 고급 위협 방지 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="52979-112">변수</span><span class="sxs-lookup"><span data-stu-id="52979-112">PARAMETERS</span></span>

### <span data-ttu-id="52979-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52979-113">-DefaultProfile</span></span>
<span data-ttu-id="52979-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="52979-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52979-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="52979-115">-EmailAdmins</span></span>
<span data-ttu-id="52979-116">고급 위협 방지 설정이 전자 메일을 사용 하 여 관리자에 게 연락 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="52979-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="52979-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="52979-118">설정에서 제외할 검색 유형의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="52979-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="52979-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52979-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="52979-120">Sql_Injection</span></span>
- <span data-ttu-id="52979-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="52979-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="52979-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="52979-122">Access_Anomaly</span></span>
- <span data-ttu-id="52979-123">않아야</span><span class="sxs-lookup"><span data-stu-id="52979-123">None</span></span>

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

### <span data-ttu-id="52979-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="52979-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="52979-125">설정이 알림을 보내는 세미콜론으로 구분 된 전자 메일 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="52979-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52979-126">-PassThru</span></span>
<span data-ttu-id="52979-127">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52979-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52979-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52979-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52979-129">-ResourceGroupName</span></span>
<span data-ttu-id="52979-130">서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="52979-131">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="52979-131">-RetentionInDays</span></span>
<span data-ttu-id="52979-132">감사 로그 보존 일 수</span><span class="sxs-lookup"><span data-stu-id="52979-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="52979-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52979-133">-ServerName</span></span>
<span data-ttu-id="52979-134">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="52979-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="52979-135">-StorageAccountName</span></span>
<span data-ttu-id="52979-136">사용할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="52979-137">와일드 카드는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52979-137">Wildcards are not permitted.</span></span> <span data-ttu-id="52979-138">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52979-138">This parameter is not required.</span></span> <span data-ttu-id="52979-139">이 매개 변수를 제공 하지 않으면 cmdlet은 이전에 데이터베이스의 고급 위협 보호 설정의 일부로 정의 된 저장소 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="52979-140">데이터베이스 위협 검색 설정을 처음 정의 하 고이 매개 변수를 제공 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="52979-141">-확인</span><span class="sxs-lookup"><span data-stu-id="52979-141">-Confirm</span></span>
<span data-ttu-id="52979-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52979-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52979-143">-WhatIf</span></span>
<span data-ttu-id="52979-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52979-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52979-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52979-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52979-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52979-146">CommonParameters</span></span>
<span data-ttu-id="52979-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52979-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52979-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52979-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52979-149">입력</span><span class="sxs-lookup"><span data-stu-id="52979-149">INPUTS</span></span>

### <span data-ttu-id="52979-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52979-150">System.String</span></span>

### <span data-ttu-id="52979-151">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52979-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="52979-152">ThreatDetection. DetectionType []/. \*</span><span class="sxs-lookup"><span data-stu-id="52979-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="52979-153">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52979-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52979-154">출력</span><span class="sxs-lookup"><span data-stu-id="52979-154">OUTPUTS</span></span>

### <span data-ttu-id="52979-155">ThreatDetection. ServerThreatDetectionsettingsModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="52979-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="52979-156">상속자</span><span class="sxs-lookup"><span data-stu-id="52979-156">NOTES</span></span>

## <span data-ttu-id="52979-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52979-157">RELATED LINKS</span></span>

[<span data-ttu-id="52979-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="52979-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="52979-159">제거-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="52979-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="52979-160">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="52979-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
