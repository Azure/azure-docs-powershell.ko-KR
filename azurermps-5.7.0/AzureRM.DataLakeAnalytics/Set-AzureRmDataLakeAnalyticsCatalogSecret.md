---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: cce57a2437a5e1fa0f440986534a11c1ab6c73ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529855"
---
# <span data-ttu-id="88388-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="88388-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="88388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88388-102">SYNOPSIS</span></span>
<span data-ttu-id="88388-103">Data Lake Analytics 카탈로그 비밀을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88388-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88388-104">SYNTAX</span></span>

### <span data-ttu-id="88388-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="88388-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88388-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="88388-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88388-107">설명은</span><span class="sxs-lookup"><span data-stu-id="88388-107">DESCRIPTION</span></span>
<span data-ttu-id="88388-108">**AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet은 Azure Data Lake Analytics 카탈로그와 관련 된 암호를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="88388-109">예제의</span><span class="sxs-lookup"><span data-stu-id="88388-109">EXAMPLES</span></span>

### <span data-ttu-id="88388-110">예제 1: 계정과 연결 된 비밀 수정</span><span class="sxs-lookup"><span data-stu-id="88388-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="88388-111">이 명령은 Data Lake Analytics 카탈로그와 관련 된 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="88388-112">변수</span><span class="sxs-lookup"><span data-stu-id="88388-112">PARAMETERS</span></span>

### <span data-ttu-id="88388-113">-계정</span><span class="sxs-lookup"><span data-stu-id="88388-113">-Account</span></span>
<span data-ttu-id="88388-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="88388-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="88388-115">-DatabaseHost</span></span>
<span data-ttu-id="88388-116">비밀이 연결 되는 데이터베이스의 호스트 이름을 ' mydatabase.contoso.com ' 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88388-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88388-117">-DatabaseName</span></span>
<span data-ttu-id="88388-118">비밀을 보유 하 고 있는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="88388-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88388-119">-DefaultProfile</span></span>
<span data-ttu-id="88388-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88388-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88388-121">-포트</span><span class="sxs-lookup"><span data-stu-id="88388-121">-Port</span></span>
<span data-ttu-id="88388-122">비밀의 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullUri
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88388-123">-비밀</span><span class="sxs-lookup"><span data-stu-id="88388-123">-Secret</span></span>
<span data-ttu-id="88388-124">비밀의 이름과 비밀 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88388-125">-Uri</span><span class="sxs-lookup"><span data-stu-id="88388-125">-Uri</span></span>
<span data-ttu-id="88388-126">비밀에 대 한 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88388-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88388-127">CommonParameters</span></span>
<span data-ttu-id="88388-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88388-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88388-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88388-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88388-130">입력</span><span class="sxs-lookup"><span data-stu-id="88388-130">INPUTS</span></span>

### <span data-ttu-id="88388-131">않아야</span><span class="sxs-lookup"><span data-stu-id="88388-131">None</span></span>
<span data-ttu-id="88388-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88388-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88388-133">출력</span><span class="sxs-lookup"><span data-stu-id="88388-133">OUTPUTS</span></span>

### <span data-ttu-id="88388-134">않아야</span><span class="sxs-lookup"><span data-stu-id="88388-134">None</span></span>

## <span data-ttu-id="88388-135">상속자</span><span class="sxs-lookup"><span data-stu-id="88388-135">NOTES</span></span>

## <span data-ttu-id="88388-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88388-136">RELATED LINKS</span></span>

[<span data-ttu-id="88388-137">새로운 AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="88388-137">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="88388-138">제거-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="88388-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


