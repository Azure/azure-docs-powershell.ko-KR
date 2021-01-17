---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353193"
---
# <span data-ttu-id="ef198-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="ef198-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="ef198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef198-102">SYNOPSIS</span></span>
<span data-ttu-id="ef198-103">새 Azure Data Lake Analytics 카탈로그 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="ef198-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef198-104">SYNTAX</span></span>

### <span data-ttu-id="ef198-105">CreateByHostNameAndPort(기본값)</span><span class="sxs-lookup"><span data-stu-id="ef198-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef198-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="ef198-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef198-107">설명</span><span class="sxs-lookup"><span data-stu-id="ef198-107">DESCRIPTION</span></span>
<span data-ttu-id="ef198-108">이 New-AzDataLakeAnalyticsCatalogCredential cmdlet은 외부 데이터 원본에 연결하기 위해 Azure Data Lake Analytics 카탈로그에서 사용할 새 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="ef198-109">예제</span><span class="sxs-lookup"><span data-stu-id="ef198-109">EXAMPLES</span></span>

### <span data-ttu-id="ef198-110">예제 1: 호스트 및 포트를 지정하는 카탈로그에 대한 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="ef198-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="ef198-111">이 명령은 https 프로토콜을 사용하여 지정된 계정, 데이터베이스, 호스트 및 포트에 대해 지정된 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="ef198-112">예제 2: 전체 URI를 지정하는 카탈로그에 대한 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="ef198-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="ef198-113">이 명령은 지정된 계정, 데이터베이스 및 외부 데이터 원본 URI에 대해 지정된 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="ef198-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef198-114">PARAMETERS</span></span>

### <span data-ttu-id="ef198-115">-Account</span><span class="sxs-lookup"><span data-stu-id="ef198-115">-Account</span></span>
<span data-ttu-id="ef198-116">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef198-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="ef198-117">-Credential</span></span>
<span data-ttu-id="ef198-118">자격 증명의 사용자 이름 및 해당 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef198-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ef198-119">-CredentialName</span></span>
<span data-ttu-id="ef198-120">자격 증명의 이름 및 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="ef198-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="ef198-121">-DatabaseHost</span></span>
<span data-ttu-id="ef198-122">자격 증명이 연결할 수 있는 외부 데이터 원본의 호스트 이름을 mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ef198-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef198-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef198-123">-DatabaseName</span></span>
<span data-ttu-id="ef198-124">자격 증명이 저장될 Data Lake Analytics 계정의 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="ef198-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef198-125">-DefaultProfile</span></span>
<span data-ttu-id="ef198-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ef198-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef198-127">-Port</span><span class="sxs-lookup"><span data-stu-id="ef198-127">-Port</span></span>
<span data-ttu-id="ef198-128">이 자격 증명을 사용하여 지정된 DatabaseHost에 연결하는 데 사용되는 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef198-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="ef198-129">-Uri</span></span>
<span data-ttu-id="ef198-130">이 자격 증명이 연결할 수 있는 외부 데이터 원본의 전체 URI(Uniform Resource Identifier)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef198-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef198-131">-Confirm</span></span>
<span data-ttu-id="ef198-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef198-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef198-133">-WhatIf</span></span>
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

### <span data-ttu-id="ef198-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef198-134">CommonParameters</span></span>
<span data-ttu-id="ef198-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef198-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef198-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ef198-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef198-137">입력</span><span class="sxs-lookup"><span data-stu-id="ef198-137">INPUTS</span></span>

### <span data-ttu-id="ef198-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ef198-138">System.String</span></span>

### <span data-ttu-id="ef198-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="ef198-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ef198-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="ef198-140">System.Uri</span></span>

### <span data-ttu-id="ef198-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ef198-141">System.Int32</span></span>

## <span data-ttu-id="ef198-142">출력</span><span class="sxs-lookup"><span data-stu-id="ef198-142">OUTPUTS</span></span>

### <span data-ttu-id="ef198-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="ef198-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="ef198-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef198-144">NOTES</span></span>

## <span data-ttu-id="ef198-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef198-145">RELATED LINKS</span></span>
