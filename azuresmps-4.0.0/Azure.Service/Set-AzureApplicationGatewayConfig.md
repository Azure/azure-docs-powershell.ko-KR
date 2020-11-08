---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046429"
---
# <span data-ttu-id="674ef-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="674ef-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="674ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="674ef-102">SYNOPSIS</span></span>
<span data-ttu-id="674ef-103">응용 프로그램 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-103">Configures an application gateway.</span></span>

## <span data-ttu-id="674ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="674ef-104">SYNTAX</span></span>

### <span data-ttu-id="674ef-105">Read-configfile</span><span class="sxs-lookup"><span data-stu-id="674ef-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="674ef-106">configObject</span><span class="sxs-lookup"><span data-stu-id="674ef-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="674ef-107">설명은</span><span class="sxs-lookup"><span data-stu-id="674ef-107">DESCRIPTION</span></span>
<span data-ttu-id="674ef-108">**Set-Azureapplication의 config** cmdlet은 응용 프로그램 게이트웨이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="674ef-109">예제의</span><span class="sxs-lookup"><span data-stu-id="674ef-109">EXAMPLES</span></span>

### <span data-ttu-id="674ef-110">예제 1: 구성 개체를 사용 하 여 응용 프로그램 게이트웨이 구성</span><span class="sxs-lookup"><span data-stu-id="674ef-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="674ef-111">첫 번째 명령은 **Get AzureapplicationApplicationGateway02 config** cmdlet을 사용 하 여 라는 응용 프로그램 게이트웨이에 대 한 구성 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="674ef-112">명령이 $ConfigReturnObject 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="674ef-113">두 번째 명령은 $ConfigReturnObject 변수에 저장 된 응용 프로그램 게이트웨이 구성 개체를 사용 하 여 ApplicationGateway06 라는 응용 프로그램에 대 한 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="674ef-114">예제 2: 구성 파일을 사용 하 여 응용 프로그램 게이트웨이 구성</span><span class="sxs-lookup"><span data-stu-id="674ef-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="674ef-115">이 명령은 지정 된 위치에서 응용 프로그램 게이트웨이 구성 파일을 사용 하 여 ApplicationGateway06 이라는 응용 프로그램에 대 한 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="674ef-116">예제 3: 구성 개체를 사용 하 여 구성 수정</span><span class="sxs-lookup"><span data-stu-id="674ef-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="674ef-117">첫 번째 명령은 **Get AzureapplicationApplicationGateway06 config** cmdlet을 사용 하 여 라는 응용 프로그램 게이트웨이에 대 한 구성 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="674ef-118">명령이 $ConfigReturnObject 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="674ef-119">두 번째 명령은 $ConfigReturnObject에 저장 된 개체의 **port** 속성에 포트 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="674ef-120">마지막 명령은 현재 cmdlet에 업데이트 된 $ConfigReturnObject을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="674ef-121">변수</span><span class="sxs-lookup"><span data-stu-id="674ef-121">PARAMETERS</span></span>

### <span data-ttu-id="674ef-122">-구성</span><span class="sxs-lookup"><span data-stu-id="674ef-122">-Config</span></span>
<span data-ttu-id="674ef-123">응용 프로그램 게이트웨이 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="674ef-124">이 cmdlet은이 매개 변수에서 지정 하는 구성을 응용 프로그램 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674ef-125">-Read-configfile</span><span class="sxs-lookup"><span data-stu-id="674ef-125">-ConfigFile</span></span>
<span data-ttu-id="674ef-126">응용 프로그램 게이트웨이의 구성 파일 경로를 XML 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="674ef-127">이 cmdlet은이 매개 변수에서 지정 하는 구성을 응용 프로그램 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674ef-128">-이름</span><span class="sxs-lookup"><span data-stu-id="674ef-128">-Name</span></span>
<span data-ttu-id="674ef-129">이 cmdlet이 구성 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674ef-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="674ef-130">-Profile</span></span>
<span data-ttu-id="674ef-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="674ef-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="674ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674ef-133">CommonParameters</span></span>
<span data-ttu-id="674ef-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="674ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674ef-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="674ef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674ef-136">입력</span><span class="sxs-lookup"><span data-stu-id="674ef-136">INPUTS</span></span>

### <span data-ttu-id="674ef-137">System.webserver, Microsoft Azure. Application게이트웨이 Objectmodel. i m a 구성</span><span class="sxs-lookup"><span data-stu-id="674ef-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="674ef-138">출력</span><span class="sxs-lookup"><span data-stu-id="674ef-138">OUTPUTS</span></span>

### <span data-ttu-id="674ef-139">WindowsAzure의. i a m a 관리 응답</span><span class="sxs-lookup"><span data-stu-id="674ef-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="674ef-140">상속자</span><span class="sxs-lookup"><span data-stu-id="674ef-140">NOTES</span></span>

## <span data-ttu-id="674ef-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="674ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="674ef-142">Get-Azureapplication게이트웨이 구성</span><span class="sxs-lookup"><span data-stu-id="674ef-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


