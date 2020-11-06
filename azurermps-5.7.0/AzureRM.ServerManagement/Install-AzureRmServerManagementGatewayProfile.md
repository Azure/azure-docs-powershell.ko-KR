---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/install-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b9563e9b8b7afb7b980f0b3cd307c76fb9c6e8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528820"
---
# <span data-ttu-id="5eb2b-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="5eb2b-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="5eb2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb2b-103">서버 관리 게이트웨이 프로필을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eb2b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5eb2b-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb2b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5eb2b-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb2b-106">**AzureRmServerManagementGatewayProfile** Cmdlet은 Azure Server Management Gateway 프로필을 올바른 위치에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="5eb2b-107">이 cmdlet이 설치 되는 파일의 이름이 profile.js설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="5eb2b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5eb2b-108">EXAMPLES</span></span>

## <span data-ttu-id="5eb2b-109">변수</span><span class="sxs-lookup"><span data-stu-id="5eb2b-109">PARAMETERS</span></span>

### <span data-ttu-id="5eb2b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb2b-110">-DefaultProfile</span></span>
<span data-ttu-id="5eb2b-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eb2b-112">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5eb2b-112">-InputFile</span></span>
<span data-ttu-id="5eb2b-113">설치할 게이트웨이 프로필을 포함 하는 로컬 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-113">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="5eb2b-114">이 cmdlet이 설치 하는 파일이 이전에 Save-AzureRmServerManagementGatewayProfile cmdlet을 사용 하 여 저장 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-114">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb2b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb2b-115">CommonParameters</span></span>
<span data-ttu-id="5eb2b-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb2b-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb2b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb2b-118">입력</span><span class="sxs-lookup"><span data-stu-id="5eb2b-118">INPUTS</span></span>

### <span data-ttu-id="5eb2b-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="5eb2b-119">FileInfo</span></span>
<span data-ttu-id="5eb2b-120">' InputFile ' 매개 변수는 파이프라인에서 ' FileInfo ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb2b-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="5eb2b-121">출력</span><span class="sxs-lookup"><span data-stu-id="5eb2b-121">OUTPUTS</span></span>

## <span data-ttu-id="5eb2b-122">상속자</span><span class="sxs-lookup"><span data-stu-id="5eb2b-122">NOTES</span></span>

## <span data-ttu-id="5eb2b-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5eb2b-123">RELATED LINKS</span></span>

[<span data-ttu-id="5eb2b-124">다시 설정-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="5eb2b-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="5eb2b-125">저장-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="5eb2b-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


