---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 2dd97b310de764638fab029c60407c578287e9a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528990"
---
# <span data-ttu-id="43f49-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="43f49-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="43f49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43f49-102">SYNOPSIS</span></span>
<span data-ttu-id="43f49-103">새 Azure Data Lake Analytics 카탈로그 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43f49-104">SYNTAX</span></span>

### <span data-ttu-id="43f49-105">CreateByHostNameAndPort (기본값)</span><span class="sxs-lookup"><span data-stu-id="43f49-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43f49-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="43f49-106">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f49-107">설명은</span><span class="sxs-lookup"><span data-stu-id="43f49-107">DESCRIPTION</span></span>
<span data-ttu-id="43f49-108">New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet은 외부 데이터 원본에 연결 하기 위해 Azure Data Lake Analytics 카탈로그에서 사용할 새 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="43f49-109">예제의</span><span class="sxs-lookup"><span data-stu-id="43f49-109">EXAMPLES</span></span>

### <span data-ttu-id="43f49-110">예제 1: 호스트 및 포트를 지정 하는 카탈로그에 대 한 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="43f49-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="43f49-111">이 명령은 https 프로토콜을 사용 하 여 지정 된 계정, 데이터베이스, 호스트 및 포트에 대해 지정 된 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="43f49-112">예제 2: 전체 URI를 지정 하는 카탈로그에 대 한 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="43f49-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="43f49-113">이 명령은 지정 된 계정, 데이터베이스 및 외부 데이터 원본 URI에 대해 지정 된 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="43f49-114">변수</span><span class="sxs-lookup"><span data-stu-id="43f49-114">PARAMETERS</span></span>

### <span data-ttu-id="43f49-115">-계정</span><span class="sxs-lookup"><span data-stu-id="43f49-115">-Account</span></span>
<span data-ttu-id="43f49-116">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="43f49-117">-Credential</span></span>
<span data-ttu-id="43f49-118">자격 증명의 사용자 이름 및 해당 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="43f49-119">-CredentialName</span></span>
<span data-ttu-id="43f49-120">자격 증명의 이름 및 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="43f49-121">-DatabaseHost</span></span>
<span data-ttu-id="43f49-122">자격 증명을 mydatabase.contoso.com 형식으로 연결할 수 있는 외부 데이터 원본의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="43f49-123">-DatabaseName</span></span>
<span data-ttu-id="43f49-124">자격 증명을 저장할 데이터 호수 분석 acocunt 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f49-125">-DefaultProfile</span></span>
<span data-ttu-id="43f49-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43f49-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43f49-127">-포트</span><span class="sxs-lookup"><span data-stu-id="43f49-127">-Port</span></span>
<span data-ttu-id="43f49-128">이 자격 증명을 사용 하 여 지정 된 DatabaseHost에 연결 하는 데 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateByFullURI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="43f49-129">-Uri</span></span>
<span data-ttu-id="43f49-130">이 자격 증명이 연결할 수 있는 외부 데이터 원본의 전체 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: Uri
Parameter Sets: CreateByHostNameAndPort
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-131">-확인</span><span class="sxs-lookup"><span data-stu-id="43f49-131">-Confirm</span></span>
<span data-ttu-id="43f49-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f49-133">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f49-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f49-134">CommonParameters</span></span>
<span data-ttu-id="43f49-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f49-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f49-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f49-137">입력</span><span class="sxs-lookup"><span data-stu-id="43f49-137">INPUTS</span></span>

### <span data-ttu-id="43f49-138">않아야</span><span class="sxs-lookup"><span data-stu-id="43f49-138">None</span></span>
<span data-ttu-id="43f49-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43f49-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43f49-140">출력</span><span class="sxs-lookup"><span data-stu-id="43f49-140">OUTPUTS</span></span>

### <span data-ttu-id="43f49-141">않아야</span><span class="sxs-lookup"><span data-stu-id="43f49-141">None</span></span>

## <span data-ttu-id="43f49-142">상속자</span><span class="sxs-lookup"><span data-stu-id="43f49-142">NOTES</span></span>

## <span data-ttu-id="43f49-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43f49-143">RELATED LINKS</span></span>

