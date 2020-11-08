---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045665"
---
# <span data-ttu-id="34d25-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="34d25-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="34d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34d25-102">SYNOPSIS</span></span>
<span data-ttu-id="34d25-103">응용 프로그램 게이트웨이 구성 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="34d25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34d25-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="34d25-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34d25-105">DESCRIPTION</span></span>
<span data-ttu-id="34d25-106">**Get-Azureapplication의 config** Cmdlet은 Azure Application Gateway 구성 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="34d25-107">컨텍스트에는 구성 개체와 XML 구성이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="34d25-108">XML 구성을 파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="34d25-109">예제의</span><span class="sxs-lookup"><span data-stu-id="34d25-109">EXAMPLES</span></span>

### <span data-ttu-id="34d25-110">예제 1: 응용 프로그램 게이트웨이 구성 가져오기 및 파일에 저장</span><span class="sxs-lookup"><span data-stu-id="34d25-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="34d25-111">이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이에 대 한 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="34d25-112">이 명령은 지정 된 경로의 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="34d25-113">변수</span><span class="sxs-lookup"><span data-stu-id="34d25-113">PARAMETERS</span></span>

### <span data-ttu-id="34d25-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="34d25-114">-ExportToFile</span></span>
<span data-ttu-id="34d25-115">이 cmdlet이 구성을 XML 형식으로 저장 하는 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d25-116">-이름</span><span class="sxs-lookup"><span data-stu-id="34d25-116">-Name</span></span>
<span data-ttu-id="34d25-117">이 cmdlet이 구성 정보를 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34d25-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="34d25-118">-Profile</span></span>
<span data-ttu-id="34d25-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="34d25-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d25-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d25-121">CommonParameters</span></span>
<span data-ttu-id="34d25-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d25-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d25-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d25-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d25-124">입력</span><span class="sxs-lookup"><span data-stu-id="34d25-124">INPUTS</span></span>

### <span data-ttu-id="34d25-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34d25-125">System.String</span></span>

## <span data-ttu-id="34d25-126">출력</span><span class="sxs-lookup"><span data-stu-id="34d25-126">OUTPUTS</span></span>

### <span data-ttu-id="34d25-127">Microsoft. Azure. i m m.</span><span class="sxs-lookup"><span data-stu-id="34d25-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="34d25-128">상속자</span><span class="sxs-lookup"><span data-stu-id="34d25-128">NOTES</span></span>

## <span data-ttu-id="34d25-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34d25-129">RELATED LINKS</span></span>

[<span data-ttu-id="34d25-130">Set-Azureapplication게이트웨이 구성</span><span class="sxs-lookup"><span data-stu-id="34d25-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


