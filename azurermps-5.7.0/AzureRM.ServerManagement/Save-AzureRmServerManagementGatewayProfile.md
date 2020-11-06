---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/save-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 8dd9aeaaf987fba155ca80b0c8739d44c80945e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528810"
---
# <span data-ttu-id="db508-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="db508-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="db508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db508-102">SYNOPSIS</span></span>
<span data-ttu-id="db508-103">서버 관리 게이트웨이의 프로필을 다운로드 하 여 로컬 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db508-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db508-104">SYNTAX</span></span>

### <span data-ttu-id="db508-105">ByName</span><span class="sxs-lookup"><span data-stu-id="db508-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db508-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="db508-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db508-107">설명은</span><span class="sxs-lookup"><span data-stu-id="db508-107">DESCRIPTION</span></span>
<span data-ttu-id="db508-108">**AzureRmServerManagementGatewayProfile** Cmdlet은 Azure 서버 관리 게이트웨이의 프로필을 다운로드 하 여 로컬 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="db508-109">예제의</span><span class="sxs-lookup"><span data-stu-id="db508-109">EXAMPLES</span></span>

## <span data-ttu-id="db508-110">변수</span><span class="sxs-lookup"><span data-stu-id="db508-110">PARAMETERS</span></span>

### <span data-ttu-id="db508-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db508-111">-DefaultProfile</span></span>
<span data-ttu-id="db508-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db508-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db508-113">-게이트웨이</span><span class="sxs-lookup"><span data-stu-id="db508-113">-Gateway</span></span>
<span data-ttu-id="db508-114">이 cmdlet이 프로필을 가져오는 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-114">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="db508-115">ResourceGroupName 및 게이트웨이 이름을 지정 하는 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db508-115">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db508-116">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="db508-116">-GatewayName</span></span>
<span data-ttu-id="db508-117">이 cmdlet이 프로필을 가져오는 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-117">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db508-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="db508-118">-OutputFile</span></span>
<span data-ttu-id="db508-119">프로필 데이터를 저장할 로컬 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-119">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db508-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db508-120">-ResourceGroupName</span></span>
<span data-ttu-id="db508-121">게이트웨이가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-121">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db508-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db508-122">CommonParameters</span></span>
<span data-ttu-id="db508-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db508-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db508-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db508-125">입력</span><span class="sxs-lookup"><span data-stu-id="db508-125">INPUTS</span></span>

### <span data-ttu-id="db508-126">게이트웨이와</span><span class="sxs-lookup"><span data-stu-id="db508-126">Gateway</span></span>
<span data-ttu-id="db508-127">' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db508-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="db508-128">출력</span><span class="sxs-lookup"><span data-stu-id="db508-128">OUTPUTS</span></span>

### <span data-ttu-id="db508-129">시스템. o. FileInfo</span><span class="sxs-lookup"><span data-stu-id="db508-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="db508-130">상속자</span><span class="sxs-lookup"><span data-stu-id="db508-130">NOTES</span></span>

## <span data-ttu-id="db508-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db508-131">RELATED LINKS</span></span>

[<span data-ttu-id="db508-132">설치-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="db508-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="db508-133">다시 설정-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="db508-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


